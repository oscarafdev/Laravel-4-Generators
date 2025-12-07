## ?????????

| ?? / ?? | ??? Laravel ?? | ??? PHP ?? | ?? |
|-------------|---------------------|-----------------|------|
| laravel-9.x(?? 9.0.0) | 9.x | >= 8.0.2 | ?? composer require oscarafdev/laravel-4-generators:^9.0 ????? Laravel 9 ?????????????? |
| 2.x ??(?? 2.0.24) | 5.x � 8.x | ^5.6 &#124;&#124; ^7.0 &#124;&#124; ^8.0 | ?? Laravel ???????? 2.x ??? |

? master ??? Laravel 10+ ?,????? laravel-9.x ????? 9.x ??(??????? 9.y.z ??)?
# 使用自定义代码生成工具快速进行Laravel开发

[![Build Status](https://travis-ci.org/JeffreyWay/Laravel-4-Generators.png?branch=master)](https://travis-ci.org/JeffreyWay/Laravel-4-Generators)

这个Laravle包提供了一种代码生成器，使得你可以加速你的开发进程，这些生成器包括：

- `generate:model`   - 模型生成器
- `generate:view`    - 视图生成器
- `generate:controller`  - 控制器生成器
- `generate:seed`    - 数据库填充器
- `generate:migration`   - 迁移
- `generate:pivot`   - 关联表
- `generate:resource` -资源
- `generate:scaffold` - 脚手架


## 安装

> [需要一个五分钟教程视频吗?](https://dl.dropboxusercontent.com/u/774859/Work/Laravel-4-Generators/Get-Started-With-Laravel-Custom-Generators.mp4)

## Laravel 4.2 或者更低的版本

使用Composer安装这个包，编辑你项目的`composer.json`文件，在require中添加`way/generators`

    "require-dev": {
		"way/generators": "~2.0"
	}

然后，在命令行下执行composer update：

    composer update --dev

一旦这个操作完成，就只需要最后一步，在配置文件中加入服务提供者。打开`app/config/app.php`文件，添加一个新的记录到providers数组中.

    'Way\Generators\GeneratorsServiceProvider'

这样就可以了，你已经安装完成并可以运行这个包了。运行artisan命令行则可以在终端上看到generate相关命令。

    php artisan

## Laravel 5.0 或者更高版本

使用Composer安装这个包，编辑你项目的`composer.json`文件，在require中添加`way/generators`

	"require-dev": {
		"way/generators": "~3.0"
	}
由于在Laravel高版本中默认文件夹结构，需要3.0或者更高的版本，才能适应5.0版本以上的Laravel

然后，在命令行下执行composer update：

    composer update --dev

一旦这个操作完成，就只需要最后一步，在配置文件中加入服务提供者。打开`app/config/app.php`文件，添加一个新的记录到providers数组中.

    'Way\Generators\GeneratorsServiceProvider'

这样就可以了，你已经安装完成并可以运行这个包了。运行artisan命令行则可以在终端上看到generate相关命令。

    php artisan

## 使用示例

想象一下使用一个生成器加速你的工作流。而不是打开models文件夹，创建一个新的文件，保存它，并且在文件中添加一个class，你可以简单的运行一个生成器命令即可完成这一系列动作。

- [Migrations 迁移](#migrations)
- [Models 模型](#models)
- [Views 视图](#views)
- [Seeds 填充](#seeds)
- [Pivot 关联表](#pivot)
- [Resources 资源](#resources)
- [Scaffolding 脚手架](#scaffolding)
- [Configuration 配置](#configuration)

### 迁移

Laravel提供了一个迁移生成器，但是它仅仅能够创建数据库结构。让我们再回顾几个例子，使用`generate:migration`。

    php artisan generate:migration create_posts_table

如果我们不指定字段配置项，则下面这个文件将被创建在`app/database/migrations`目录下。

```php
<?php

use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;

class CreatePostsTable extends Migration {

	/**
	 * Run the migrations.
	 *
	 * @return void
	 */
	public function up()
	{
        Schema::create('posts', function(Blueprint $table) {
            $table->increments('id');
            $table->timestamps();
        });
	}

	/**
	 * Reverse the migrations.
	 *
	 * @return void
	 */
	public function down()
	{
	    Schema::drop('posts');
	}

}

```

注意，生成器能够检测到你正在尝试创建一个表。迁移的名称，尽量应该是可描述的。生成器将扫描你的生成器名字的第一个单词，并尽力确定如何继续。例如，对于迁移`create_posts_table`，关键字"create"，意味着我们应该准备必要的架构来创建表。

如果你使用`add_user_id_to_posts_table`代替迁移的名字，在上面的示例中，关键字"add"，意味着我们将添加一行到现有的表中，然我们看看这个生成器命令。

    php artisan generate:migration add_user_id_to_posts_table

这个命令将会准备一个下面这样的样板：


```php
<?php

use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;

class AddUserIdToPostsTable extends Migration {

	/**
	 * Run the migrations.
	 *
	 * @return void
	 */
	public function up()
	{
        Schema::table('posts', function(Blueprint $table) {

        });
	}


	/**
	 * Reverse the migrations.
	 *
	 * @return void
	 */
	public function down()
	{
	    Schema::table('posts', function(Blueprint $table) {

        });
	}

}
```

注意：这一次我们没有做`Schema::create`

#### 关键字

当你在写迁移的名字的时候，使用下面的关键字给生成器提供提示。

- `create` or `make` (`create_users_table`)
- `add` or `insert` (`add_user_id_to_posts_table`)
- `remove` (`remove_user_id_from_posts_table`)
- `delete` or `drop` (`delete_users_table`)

#### 生成数据库模式

这是非常漂亮的，但是让我们更进一步，生成数据库模式的同时，使用`fields`选项。

    php artisan generate:migration create_posts_table --fields="title:string, body:text"

在我们解释这个选项之前，让我们先看一下输出：

```php
<?php

use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;

class CreatePostsTable extends Migration {

	/**
	 * Run the migrations.
	 *
	 * @return void
	 */
	public function up()
	{
        Schema::create('posts', function(Blueprint $table) {
            $table->increments('id');
            $table->string('title');
			$table->text('body');
			$table->timestamps();
        });
	}

	/**
	 * Reverse the migrations.
	 *
	 * @return void
	 */
	public function down()
	{
	    Schema::drop('posts');
	}

}
```

漂亮！少量的提示在这里：

- 生成器将默认使用自增的`id`字段作为主键
- 它解析`fields`选项，并添加这些字段
- drop方法能够足够聪明的意识到，在相反的情况下，这个表应该被完全删除

声明字段，使用逗号+空格分隔键值列表[key:value:option sets]，其中`key`表示字段的名称，`value`表示[字段的类型](http://laravel.com/docs/schema#adding-columns)，`option`表示制定索引或者像是`unique`、`nullable`这样的属性。
这里是一些示例:

- `--fields="first:string, last:string"`
- `--fields="age:integer, yob:date"`
- `--fields="username:string:unique, age:integer:nullable"`
- `--fields="name:string:default('John Doe'), bio:text:nullable"`
- `--fields="username:string(30):unique, age:integer:nullable:default(18)"`

请注意最后一个示例，这里我们指定了`string(30)`的字符串限制。这将产生`$table->string('username', 30)->unique();`

使用生成器删除表是可能的：

	php artisan generate:migration delete_posts_table

作为最后一个示例i，让我们运行一个迁移，从`tasks`表中，删除`completed`字段。

    php artisan generate:migration remove_completed_from_tasks_table --fields="completed:boolean"

这一次，我们使用了"remove"关键字，生成器知道它要删除一个字段，并且把它添加到`down()`方法中。

```php
<?php

use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;

class RemoveCompletedFromTasksTable extends Migration {

	/**
	 * Run the migrations.
	 *
	 * @return void
	 */
	public function up()
	{
        Schema::table('tasks', function(Blueprint $table) {
            $table->dropColumn('completed');
        });
	}


	/**
	 * Reverse the migrations.
	 *
	 * @return void
	 */
	public function down()
	{
	    Schema::table('tasks', function(Blueprint $table) {
            $table->boolean('completed');
        });
	}

}
```

### 模型

    php artisan generate:model Post

这将生成一个文件，`app/models/Post.php`并且写入下面的样板

```php
<?php

class Post extends \Eloquent {

}
```

### 视图

视图生成器相当简单。

```bash
php artisan generate:view admin.reports.index
```

这个命令将创建一个空的视图，`/app/views/admin/reports/index.blade.php`。如果提供的文件夹不存在，它会自动帮你创建

### Seeds 生成数据[译注：应该是用来填充测试数据]

Laravel为我们提供了非常灵活的方式来填充表
Laravel provides us with a flexible way to seed new tables.

    php artisan generate:seed users

设置你想要生成的生成文件参数。这将生成 `app/database/seeds/UsersTableSeeder.php` 并用一下内容作为填充：

```php
<?php

// Composer: "fzaninotto/faker": "v1.3.0"
use Faker\Factory as Faker;

class UsersTableSeeder extends Seeder {

    public function run()
    {
        $faker = Faker::create();

        foreach(range(1, 10) as $index)
        {
            User::create([

            ]);
        }
    }

}
```

这将使用流行的Faker库为你提供一个基本的样板。这将是一个非常漂亮的方式来生成你的数据库表。不要忘记使用Composer来安装Faker！

### 关联表[译注：pivot 这个词愿意是中心点、中枢的意思，这里翻译成关联表比较合适，通俗一点就是两个表的mapping关系表，带有外键约束]
当你需要一个关联表时，`generate:pivot`可以加速建立相应的表。

简单的传递两个需要关联的表的名字。对于`orders`和`users`表，你可以：

```bash
php artisan generate:pivot orders users
```

这个命令将创建下面的迁移：

```php
<?php

use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;

class CreateOrderUserTable extends Migration {

	/**
	 * Run the migrations.
	 *
	 * @return void
	 */
	public function up()
	{
        Schema::create('order_user', function(Blueprint $table) {
            $table->increments('id');
			$table->integer('order_id')->unsigned()->index();
			$table->foreign('order_id')->references('id')->on('orders')->onDelete('cascade');
			$table->integer('user_id')->unsigned()->index();
			$table->foreign('user_id')->references('id')->on('users')->onDelete('cascade');
			$table->timestamps();
        });
	}


	/**
	 * Reverse the migrations.
	 *
	 * @return void
	 */
	public function down()
	{
	    Schema::drop('order_user');
	}

}
```

注意，它会正确设置你提供的两个表名，排名不分先后。现在，运行`php artisan migrate`来创建你的关联表！

### 资源

`generate:resource`命令将会为你坐一系列的事情：

- 生成一个模型
- 生成index, show, create, edit视图
- 生成一个控制器
- 生成一个数据库结构迁移
- 生成一个数据库填充
- 迁移这个数据库

当你触发这个命令，它将对每个动作进行问询。通过这个方式，你可以告诉生成器，哪些是你确实需要的。

#### 例子

想象如果你需要创建一个方法来显示文章。你需要手动创建一个控制器，一个模型，一个数据库迁移并且填充它，并且创建一个数据库填充...为什么不用生成器来做呢？

```bash
php artisan generate:resource post --fields="title:string, body:text"
```

如果你对每个询问说yes，这个命令会给你如下样板：

- app/models/Post.php
- app/controllers/PostsController.php
- app/database/migrations/timestamp-create_posts_table.php (including the schema)
- app/database/seeds/PostsTableSeeder.php

### Scaffolding 脚手架

脚手架生成器类似于`generate:resource`，除了创建一些初始化样板外，同时也是为了方便。

例如，在运行`generate:scaffold post`时，你的控制器模板将会将会是：

```php
<?php

class PostsController extends \BaseController {

	/**
	 * Display a listing of posts
	 *
	 * @return Response
	 */
	public function index()
	{
	    $posts = Post::all();

	    return View::make('posts.index', compact('posts'));
	}

	/**
	 * Show the form for creating a new post
	 *
	 * @return Response
	 */
	public function create()
	{
        return View::make('posts.create');
	}

	/**
	 * Store a newly created post in storage.
	 *
	 * @return Response
	 */
	public function store()
	{
	    $validator = Validator::make($data = Input::all(), Post::$rules);

	    if ($validator->fails())
	    {
	        return Redirect::back()->withErrors($validator)->withInput();
	    }

	    Post::create($data);

	    return Redirect::route('posts.index');
	}

	/**
	 * Display the specified post.
	 *
	 * @param  int  $id
	 * @return Response
	 */
	public function show($id)
	{
	    $post = Post::findOrFail($id);

	    return View::make('posts.show', compact('post'));
	}

	/**
	 * Show the form for editing the specified post.
	 *
	 * @param  int  $id
	 * @return Response
	 */
	public function edit($id)
	{
		$post = Post::find($id);

		return View::make('posts.edit', compact('post'));
	}

	/**
	 * Update the specified resource in storage.
	 *
	 * @param  int  $id
	 * @return Response
	 */
	public function update($id)
	{
		$post = Post::findOrFail($id);

		$validator = Validator::make($data = Input::all(), Post::$rules);

        if ($validator->fails())
        {
            return Redirect::back()->withErrors($validator)->withInput();
        }

		$post->update($data);

		return Redirect::route('posts.index');
	}

	/**
	 * Remove the specified resource from storage.
	 *
	 * @param  int  $id
	 * @return Response
	 */
	public function destroy($id)
	{
		Post::destroy($id);

		return Redirect::route('posts.index');
	}

}
```

请注意我们鼓励您去修改这些自动生成的控制器。它只是一个简单的开始。

### Configuration 配置

你或许想修改你的模板--自动生成的文件是怎样格式化的。考虑到这一点，你需要发布你的模板，生成器将会使用它们。

```bash
php artisan generate:publish-templates
```

你要复制所有`app/templates`目录下的模板。你可以修改这些只要你满意它的格式。如果你喜欢不同的目录：

```bash
php artisan generate:publish-templates --path=app/foo/bar/templates
```

当你运行`generate:publish-templates` ,它也会将配置发布到`app/config/packages/way/generators/config/config.php`文件。这个文件看起来有点像：

```php
<?php

return [

    /*
    |--------------------------------------------------------------------------
    | Where the templates for the generators are stored...
    |--------------------------------------------------------------------------
    |
    */
    'model_template_path' => '/Users/jeffreyway/Desktop/generators-testing/app/templates/model.txt',

    'scaffold_model_template_path' => '/Users/jeffreyway/Desktop/generators-testing/app/templates/scaffolding/model.txt',

    'controller_template_path' => '/Users/jeffreyway/Desktop/generators-testing/app/templates/controller.txt',

    'scaffold_controller_template_path' => '/Users/jeffreyway/Desktop/generators-testing/app/templates/scaffolding/controller.txt',

    'migration_template_path' => '/Users/jeffreyway/Desktop/generators-testing/app/templates/migration.txt',

    'seed_template_path' => '/Users/jeffreyway/Desktop/generators-testing/app/templates/seed.txt',

    'view_template_path' => '/Users/jeffreyway/Desktop/generators-testing/app/templates/view.txt',


    /*
    |--------------------------------------------------------------------------
    | Where the generated files will be saved...
    |--------------------------------------------------------------------------
    |
    */
    'model_target_path'   => app_path('models'),

    'controller_target_path'   => app_path('controllers'),

    'migration_target_path'   => app_path('database/migrations'),

    'seed_target_path'   => app_path('database/seeds'),

    'view_target_path'   => app_path('views')

];
```

同时，当你修改这个文件的时候，注意你也可以更新每个默认的生成器目标目录。

### Shortcuts 快捷命令

因为你可能会一次又一次的键入如下命令，命令别名显然是有意义的。

```bash
# Generator Stuff
alias g:m="php artisan generate:model"
alias g:c="php artisan generate:controller"
alias g:v="php artisan generate:view"
alias g:s="php artisan generate:seed"
alias g:mig="php artisan generate:migration"
alias g:r="php artisan generate:resource"
```
这些将被保存，例如，你的`~/.bash_profile` 或者 `~/.bashrc` 文件中。




















