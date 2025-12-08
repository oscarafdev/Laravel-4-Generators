## ?????????

| ?? / ?? | ??? Laravel ?? | ??? PHP ?? | ?? |
|-------------|---------------------|-----------------|------|
| laravel-12.x??? 12.0.0? | 12.x | >= 8.3 | ?? `composer require oscarafdev/laravel-4-generators:^12.0` ???|
| laravel-11.x??? 11.0.0? | 11.x | >= 8.2 | `composer require oscarafdev/laravel-4-generators:^11.0`?|
| laravel-10.x??? 10.0.0? | 10.x | >= 8.1 | `composer require oscarafdev/laravel-4-generators:^10.0`?|
| laravel-9.x??? 9.0.0? | 9.x | >= 8.0.2 | `composer require oscarafdev/laravel-4-generators:^9.0`?|
| 2.x??? 2.0.24? | 5.x - 8.x | ^5.6 || ^7.0 || ^8.0 | ?? Laravel ???|

master ????????? Laravel ?????????????? `laravel-<major>.x` ??????? `x.y.z` ???

# ?????????

| ?? / ?? | ??? Laravel ?? | ??? PHP ?? | ?? |
|-------------|---------------------|-----------------|------|
| laravel-10.x(?? 10.0.0) | 10.x | >= 8.1 | ?? composer require oscarafdev/laravel-4-generators:^10.0 ????? Laravel 10 ????????????? |
| laravel-9.x(?? 9.0.0) | 9.x | >= 8.0.2 | ?? composer require oscarafdev/laravel-4-generators:^9.0 ????? Laravel 9 ?????????????? |
| 2.x ??(?? 2.0.24) | 5.x  8.x | ^5.6 &#124;&#124; ^7.0 &#124;&#124; ^8.0 | ?? Laravel ???????? 2.x ??? |

? master ??? Laravel 10+ ?,????? laravel-9.x ????? 9.x ??(??????? 9.y.z ??)?
# 菴ｿ逕ｨ閾ｪ螳壻ｹ我ｻ｣遐∫函謌仙ｷ･蜈ｷ蠢ｫ騾溯ｿ幄｡鍬aravel蠑蜿

[![Build Status](https://travis-ci.org/JeffreyWay/Laravel-4-Generators.png?branch=master)](https://travis-ci.org/JeffreyWay/Laravel-4-Generators)

霑吩ｸｪLaravle蛹�署萓帑ｺ�ｸ遘堺ｻ｣遐∫函謌仙勣�御ｽｿ蠕嶺ｽ蜿ｯ莉･蜉騾滉ｽ逧�ｼ蜿題ｿ帷ｨ具ｼ瑚ｿ吩ｺ帷函謌仙勣蛹�峡�

- `generate:model`   - 讓｡蝙狗函謌仙勣
- `generate:view`    - 隗�崟逕滓�蝎ｨ
- `generate:controller`  - 謗ｧ蛻ｶ蝎ｨ逕滓�蝎ｨ
- `generate:seed`    - 謨ｰ謐ｮ蠎灘｡ｫ蜈�勣
- `generate:migration`   - 霑∫ｧｻ
- `generate:pivot`   - 蜈ｳ閨碑｡ｨ
- `generate:resource` -襍�ｺ
- `generate:scaffold` - 閼壽焔譫ｶ


## 螳芽｣

> [髴隕∽ｸ荳ｪ莠泌�髓滓蕗遞玖ｧ�｢大雛?](https://dl.dropboxusercontent.com/u/774859/Work/Laravel-4-Generators/Get-Started-With-Laravel-Custom-Generators.mp4)

## Laravel 4.2 謌冶�峩菴守噪迚域悽

菴ｿ逕ｨComposer螳芽｣�ｿ吩ｸｪ蛹�ｼ檎ｼ冶ｾ台ｽ鬘ｹ逶ｮ逧Яcomposer.json`譁�ｻｶ�悟惠require荳ｭ豺ｻ蜉`way/generators`

    "require-dev": {
		"way/generators": "~2.0"
	}

辟ｶ蜷趣ｼ悟惠蜻ｽ莉､陦御ｸ区鴬陦慶omposer update�

    composer update --dev

荳譌ｦ霑吩ｸｪ謫堺ｽ懷ｮ梧��悟ｰｱ蜿ｪ髴隕∵怙蜷惹ｸ豁･�悟惠驟咲ｽｮ譁�ｻｶ荳ｭ蜉蜈･譛榊苅謠蝉ｾ幄�よ遠蠑`app/config/app.php`譁�ｻｶ�梧ｷｻ蜉荳荳ｪ譁ｰ逧�ｮｰ蠖募芦providers謨ｰ扈�ｸｭ.

    'Way\Generators\GeneratorsServiceProvider'

霑呎ｷ蟆ｱ蜿ｯ莉･莠�ｼ御ｽ蟾ｲ扈丞ｮ芽｣�ｮ梧�蟷ｶ蜿ｯ莉･霑占｡瑚ｿ吩ｸｪ蛹�ｺ�りｿ占｡径rtisan蜻ｽ莉､陦悟�蜿ｯ莉･蝨ｨ扈育ｫｯ荳顔恚蛻ｰgenerate逶ｸ蜈ｳ蜻ｽ莉､縲

    php artisan

## Laravel 5.0 謌冶�峩鬮倡沿譛ｬ

菴ｿ逕ｨComposer螳芽｣�ｿ吩ｸｪ蛹�ｼ檎ｼ冶ｾ台ｽ鬘ｹ逶ｮ逧Яcomposer.json`譁�ｻｶ�悟惠require荳ｭ豺ｻ蜉`way/generators`

	"require-dev": {
		"way/generators": "~3.0"
	}
逕ｱ莠主惠Laravel鬮倡沿譛ｬ荳ｭ鮟倩ｮ､譁�ｻｶ螟ｹ扈捺桷�碁怙隕3.0謌冶�峩鬮倡噪迚域悽�梧燕閭ｽ騾ょｺ5.0迚域悽莉･荳顔噪Laravel

辟ｶ蜷趣ｼ悟惠蜻ｽ莉､陦御ｸ区鴬陦慶omposer update�

    composer update --dev

荳譌ｦ霑吩ｸｪ謫堺ｽ懷ｮ梧��悟ｰｱ蜿ｪ髴隕∵怙蜷惹ｸ豁･�悟惠驟咲ｽｮ譁�ｻｶ荳ｭ蜉蜈･譛榊苅謠蝉ｾ幄�よ遠蠑`app/config/app.php`譁�ｻｶ�梧ｷｻ蜉荳荳ｪ譁ｰ逧�ｮｰ蠖募芦providers謨ｰ扈�ｸｭ.

    'Way\Generators\GeneratorsServiceProvider'

霑呎ｷ蟆ｱ蜿ｯ莉･莠�ｼ御ｽ蟾ｲ扈丞ｮ芽｣�ｮ梧�蟷ｶ蜿ｯ莉･霑占｡瑚ｿ吩ｸｪ蛹�ｺ�りｿ占｡径rtisan蜻ｽ莉､陦悟�蜿ｯ莉･蝨ｨ扈育ｫｯ荳顔恚蛻ｰgenerate逶ｸ蜈ｳ蜻ｽ莉､縲

    php artisan

## 菴ｿ逕ｨ遉ｺ萓

諠ｳ雎｡荳荳倶ｽｿ逕ｨ荳荳ｪ逕滓�蝎ｨ蜉騾滉ｽ逧�ｷ･菴懈ｵ√り御ｸ肴弍謇灘ｼmodels譁�ｻｶ螟ｹ�悟�蟒ｺ荳荳ｪ譁ｰ逧�枚莉ｶ�御ｿ晏ｭ伜ｮ�ｼ悟ｹｶ荳泌惠譁�ｻｶ荳ｭ豺ｻ蜉荳荳ｪclass�御ｽ蜿ｯ莉･邂蜊慕噪霑占｡御ｸ荳ｪ逕滓�蝎ｨ蜻ｽ莉､蜊ｳ蜿ｯ螳梧�霑吩ｸ邉ｻ蛻怜勘菴懊

- [Migrations 霑∫ｧｻ](#migrations)
- [Models 讓｡蝙犠(#models)
- [Views 隗�崟](#views)
- [Seeds 蝪ｫ蜈�(#seeds)
- [Pivot 蜈ｳ閨碑｡ｨ](#pivot)
- [Resources 襍�ｺ疹(#resources)
- [Scaffolding 閼壽焔譫ｶ](#scaffolding)
- [Configuration 驟咲ｽｮ](#configuration)

### 霑∫ｧｻ

Laravel謠蝉ｾ帑ｺ�ｸ荳ｪ霑∫ｧｻ逕滓�蝎ｨ�御ｽ�弍螳�ｻ�ｻ��螟溷�蟒ｺ謨ｰ謐ｮ蠎鍋ｻ捺桷縲りｮｩ謌台ｻｬ蜀榊屓鬘ｾ蜃荳ｪ萓句ｭ撰ｼ御ｽｿ逕ｨ`generate:migration`縲

    php artisan generate:migration create_posts_table

螯よ棡謌台ｻｬ荳肴欠螳壼ｭ玲ｮｵ驟咲ｽｮ鬘ｹ�悟�荳矩擇霑吩ｸｪ譁�ｻｶ蟆�｢ｫ蛻帛ｻｺ蝨ｨ`app/database/migrations`逶ｮ蠖穂ｸ九

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

豕ｨ諢擾ｼ檎函謌仙勣閭ｽ螟滓｣豬句芦菴豁｣蝨ｨ蟆晁ｯ募�蟒ｺ荳荳ｪ陦ｨ縲りｿ∫ｧｻ逧�錐遘ｰ�悟ｰｽ驥丞ｺ碑ｯ･譏ｯ蜿ｯ謠剰ｿｰ逧�ら函謌仙勣蟆�沖謠丈ｽ逧�函謌仙勣蜷榊ｭ礼噪隨ｬ荳荳ｪ蜊戊ｯ搾ｼ悟ｹｶ蟆ｽ蜉帷｡ｮ螳壼ｦゆｽ慕ｻｧ扈ｭ縲ゆｾ句ｦゑｼ悟ｯｹ莠手ｿ∫ｧｻ`create_posts_table`�悟�髞ｮ蟄"create"�梧э蜻ｳ逹謌台ｻｬ蠎碑ｯ･蜃�､�ｿ�ｦ∫噪譫ｶ譫�擂蛻帛ｻｺ陦ｨ縲

螯よ棡菴菴ｿ逕ｨ`add_user_id_to_posts_table`莉｣譖ｿ霑∫ｧｻ逧�錐蟄暦ｼ悟惠荳企擇逧�､ｺ萓倶ｸｭ�悟�髞ｮ蟄"add"�梧э蜻ｳ逹謌台ｻｬ蟆�ｷｻ蜉荳陦悟芦邇ｰ譛臥噪陦ｨ荳ｭ�檎┯謌台ｻｬ逵狗恚霑吩ｸｪ逕滓�蝎ｨ蜻ｽ莉､縲

    php artisan generate:migration add_user_id_to_posts_table

霑吩ｸｪ蜻ｽ莉､蟆�ｼ壼㊥螟�ｸ荳ｪ荳矩擇霑呎ｷ逧�ｷ譚ｿ�


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

豕ｨ諢擾ｼ夊ｿ吩ｸ谺｡謌台ｻｬ豐｡譛牙★`Schema::create`

#### 蜈ｳ髞ｮ蟄

蠖謎ｽ蝨ｨ蜀呵ｿ∫ｧｻ逧�錐蟄礼噪譌ｶ蛟呻ｼ御ｽｿ逕ｨ荳矩擇逧��髞ｮ蟄礼ｻ咏函謌仙勣謠蝉ｾ帶署遉ｺ縲

- `create` or `make` (`create_users_table`)
- `add` or `insert` (`add_user_id_to_posts_table`)
- `remove` (`remove_user_id_from_posts_table`)
- `delete` or `drop` (`delete_users_table`)

#### 逕滓�謨ｰ謐ｮ蠎捺ｨ｡蠑

霑呎弍髱槫ｸｸ貍ゆｺｮ逧�ｼ御ｽ�弍隶ｩ謌台ｻｬ譖ｴ霑帑ｸ豁･�檎函謌先焚謐ｮ蠎捺ｨ｡蠑冗噪蜷梧慮�御ｽｿ逕ｨ`fields`騾蛾｡ｹ縲

    php artisan generate:migration create_posts_table --fields="title:string, body:text"

蝨ｨ謌台ｻｬ隗｣驥願ｿ吩ｸｪ騾蛾｡ｹ荵句燕�瑚ｮｩ謌台ｻｬ蜈育恚荳荳玖ｾ灘��

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

貍ゆｺｮ�∝ｰ鷹㍼逧�署遉ｺ蝨ｨ霑咎㈹�

- 逕滓�蝎ｨ蟆�ｻ倩ｮ､菴ｿ逕ｨ閾ｪ蠅樒噪`id`蟄玲ｮｵ菴應ｸｺ荳ｻ髞ｮ
- 螳�ｧ｣譫秦fields`騾蛾｡ｹ�悟ｹｶ豺ｻ蜉霑吩ｺ帛ｭ玲ｮｵ
- drop譁ｹ豕戊�螟溯ｶｳ螟溯↑譏守噪諢剰ｯ�芦�悟惠逶ｸ蜿咲噪諠��荳具ｼ瑚ｿ吩ｸｪ陦ｨ蠎碑ｯ･陲ｫ螳悟�蛻髯､

螢ｰ譏主ｭ玲ｮｵ�御ｽｿ逕ｨ騾怜捷+遨ｺ譬ｼ蛻�囈髞ｮ蛟ｼ蛻苓｡ｨ[key:value:option sets]�悟�荳ｭ`key`陦ｨ遉ｺ蟄玲ｮｵ逧�錐遘ｰ�形value`陦ｨ遉ｺ[蟄玲ｮｵ逧�ｱｻ蝙犠(http://laravel.com/docs/schema#adding-columns)�形option`陦ｨ遉ｺ蛻ｶ螳夂ｴ｢蠑墓�閠�ワ譏ｯ`unique`縲～nullable`霑呎ｷ逧�ｱ樊ｧ縲
霑咎㈹譏ｯ荳莠帷､ｺ萓:

- `--fields="first:string, last:string"`
- `--fields="age:integer, yob:date"`
- `--fields="username:string:unique, age:integer:nullable"`
- `--fields="name:string:default('John Doe'), bio:text:nullable"`
- `--fields="username:string(30):unique, age:integer:nullable:default(18)"`

隸ｷ豕ｨ諢乗怙蜷惹ｸ荳ｪ遉ｺ萓具ｼ瑚ｿ咎㈹謌台ｻｬ謖�ｮ壻ｺ�string(30)`逧�ｭ礼ｬｦ荳ｲ髯仙宛縲りｿ吝ｰ�ｺｧ逕歔$table->string('username', 30)->unique();`

菴ｿ逕ｨ逕滓�蝎ｨ蛻髯､陦ｨ譏ｯ蜿ｯ閭ｽ逧�ｼ

	php artisan generate:migration delete_posts_table

菴應ｸｺ譛蜷惹ｸ荳ｪ遉ｺ萓喫�瑚ｮｩ謌台ｻｬ霑占｡御ｸ荳ｪ霑∫ｧｻ�御ｻ餐tasks`陦ｨ荳ｭ�悟唖髯､`completed`蟄玲ｮｵ縲

    php artisan generate:migration remove_completed_from_tasks_table --fields="completed:boolean"

霑吩ｸ谺｡�梧�莉ｬ菴ｿ逕ｨ莠"remove"蜈ｳ髞ｮ蟄暦ｼ檎函謌仙勣遏･驕灘ｮ�ｦ∝唖髯､荳荳ｪ蟄玲ｮｵ�悟ｹｶ荳疲滑螳�ｷｻ蜉蛻ｰ`down()`譁ｹ豕穂ｸｭ縲

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

### 讓｡蝙

    php artisan generate:model Post

霑吝ｰ�函謌蝉ｸ荳ｪ譁�ｻｶ�形app/models/Post.php`蟷ｶ荳泌�蜈･荳矩擇逧�ｷ譚ｿ

```php
<?php

class Post extends \Eloquent {

}
```

### 隗�崟

隗�崟逕滓�蝎ｨ逶ｸ蠖鍋ｮ蜊輔

```bash
php artisan generate:view admin.reports.index
```

霑吩ｸｪ蜻ｽ莉､蟆��蟒ｺ荳荳ｪ遨ｺ逧�ｧ�崟�形/app/views/admin/reports/index.blade.php`縲ょｦよ棡謠蝉ｾ帷噪譁�ｻｶ螟ｹ荳榊ｭ伜惠�悟ｮ�ｼ夊�蜉ｨ蟶ｮ菴蛻帛ｻｺ

### Seeds 逕滓�謨ｰ謐ｮ[隸第ｳｨ�壼ｺ碑ｯ･譏ｯ逕ｨ譚･蝪ｫ蜈�ｵ玖ｯ墓焚謐ｮ]

Laravel荳ｺ謌台ｻｬ謠蝉ｾ帑ｺ�撼蟶ｸ轣ｵ豢ｻ逧�婿蠑乗擂蝪ｫ蜈�｡ｨ
Laravel provides us with a flexible way to seed new tables.

    php artisan generate:seed users

隶ｾ鄂ｮ菴諠ｳ隕∫函謌千噪逕滓�譁�ｻｶ蜿よ焚縲りｿ吝ｰ�函謌 `app/database/seeds/UsersTableSeeder.php` 蟷ｶ逕ｨ荳荳句�螳ｹ菴應ｸｺ蝪ｫ蜈�ｼ

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

霑吝ｰ�ｽｿ逕ｨ豬∬｡檎噪Faker蠎謎ｸｺ菴謠蝉ｾ帑ｸ荳ｪ蝓ｺ譛ｬ逧�ｷ譚ｿ縲りｿ吝ｰ�弍荳荳ｪ髱槫ｸｸ貍ゆｺｮ逧�婿蠑乗擂逕滓�菴逧�焚謐ｮ蠎楢｡ｨ縲ゆｸ崎ｦ∝ｿ倩ｮｰ菴ｿ逕ｨComposer譚･螳芽｣�aker�

### 蜈ｳ閨碑｡ｨ[隸第ｳｨ�嗔ivot 霑吩ｸｪ隸肴�諢乗弍荳ｭ蠢�せ縲∽ｸｭ譫｢逧�э諤晢ｼ瑚ｿ咎㈹鄙ｻ隸第�蜈ｳ閨碑｡ｨ豈碑ｾ�粋騾ゑｼ碁壻ｿ嶺ｸ轤ｹ蟆ｱ譏ｯ荳､荳ｪ陦ｨ逧�apping蜈ｳ邉ｻ陦ｨ�悟ｸｦ譛牙､夜醗郤ｦ譚歉
蠖謎ｽ髴隕∽ｸ荳ｪ蜈ｳ閨碑｡ｨ譌ｶ�形generate:pivot`蜿ｯ莉･蜉騾溷ｻｺ遶狗嶌蠎皮噪陦ｨ縲

邂蜊慕噪莨騾剃ｸ､荳ｪ髴隕∝�閨皮噪陦ｨ逧�錐蟄励ょｯｹ莠餐orders`蜥形users`陦ｨ�御ｽ蜿ｯ莉･�

```bash
php artisan generate:pivot orders users
```

霑吩ｸｪ蜻ｽ莉､蟆��蟒ｺ荳矩擇逧�ｿ∫ｧｻ�

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

豕ｨ諢擾ｼ悟ｮ�ｼ壽ｭ｣遑ｮ隶ｾ鄂ｮ菴謠蝉ｾ帷噪荳､荳ｪ陦ｨ蜷搾ｼ梧賜蜷堺ｸ榊�蜈亥錘縲ら鴫蝨ｨ�瑚ｿ占｡形php artisan migrate`譚･蛻帛ｻｺ菴逧��閨碑｡ｨ�

### 襍�ｺ

`generate:resource`蜻ｽ莉､蟆�ｼ壻ｸｺ菴蝮蝉ｸ邉ｻ蛻礼噪莠区ュ�

- 逕滓�荳荳ｪ讓｡蝙
- 逕滓�index, show, create, edit隗�崟
- 逕滓�荳荳ｪ謗ｧ蛻ｶ蝎ｨ
- 逕滓�荳荳ｪ謨ｰ謐ｮ蠎鍋ｻ捺桷霑∫ｧｻ
- 逕滓�荳荳ｪ謨ｰ謐ｮ蠎灘｡ｫ蜈
- 霑∫ｧｻ霑吩ｸｪ謨ｰ謐ｮ蠎

蠖謎ｽ隗ｦ蜿題ｿ吩ｸｪ蜻ｽ莉､�悟ｮ�ｰ�ｯｹ豈丈ｸｪ蜉ｨ菴懆ｿ幄｡碁琉隸｢縲る夊ｿ�ｿ吩ｸｪ譁ｹ蠑擾ｼ御ｽ蜿ｯ莉･蜻願ｯ臥函謌仙勣�悟頭莠帶弍菴遑ｮ螳樣怙隕∫噪縲

#### 萓句ｭ

諠ｳ雎｡螯よ棡菴髴隕∝�蟒ｺ荳荳ｪ譁ｹ豕墓擂譏ｾ遉ｺ譁�ｫ縲ゆｽ髴隕∵焔蜉ｨ蛻帛ｻｺ荳荳ｪ謗ｧ蛻ｶ蝎ｨ�御ｸ荳ｪ讓｡蝙具ｼ御ｸ荳ｪ謨ｰ謐ｮ蠎楢ｿ∫ｧｻ蟷ｶ荳泌｡ｫ蜈�ｮ�ｼ悟ｹｶ荳泌�蟒ｺ荳荳ｪ謨ｰ謐ｮ蠎灘｡ｫ蜈...荳ｺ莉荵井ｸ咲畑逕滓�蝎ｨ譚･蛛壼造�

```bash
php artisan generate:resource post --fields="title:string, body:text"
```

螯よ棡菴蟇ｹ豈丈ｸｪ隸｢髣ｮ隸ｴyes�瑚ｿ吩ｸｪ蜻ｽ莉､莨夂ｻ吩ｽ螯ゆｸ区ｷ譚ｿ�

- app/models/Post.php
- app/controllers/PostsController.php
- app/database/migrations/timestamp-create_posts_table.php (including the schema)
- app/database/seeds/PostsTableSeeder.php

### Scaffolding 閼壽焔譫ｶ

閼壽焔譫ｶ逕滓�蝎ｨ邀ｻ莨ｼ莠餐generate:resource`�碁勁莠��蟒ｺ荳莠帛�蟋句喧譬ｷ譚ｿ螟厄ｼ悟酔譌ｶ荵滓弍荳ｺ莠�婿萓ｿ縲

萓句ｦゑｼ悟惠霑占｡形generate:scaffold post`譌ｶ�御ｽ逧�而蛻ｶ蝎ｨ讓｡譚ｿ蟆�ｼ壼ｰ�ｼ壽弍�

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

隸ｷ豕ｨ諢乗�莉ｬ鮠灘干謔ｨ蜴ｻ菫ｮ謾ｹ霑吩ｺ幄�蜉ｨ逕滓�逧�而蛻ｶ蝎ｨ縲ょｮ�宵譏ｯ荳荳ｪ邂蜊慕噪蠑蟋九

### Configuration 驟咲ｽｮ

菴謌冶ｮｸ諠ｳ菫ｮ謾ｹ菴逧�ｨ｡譚ｿ--閾ｪ蜉ｨ逕滓�逧�枚莉ｶ譏ｯ諤取ｷ譬ｼ蠑丞喧逧�り�剔蛻ｰ霑吩ｸ轤ｹ�御ｽ髴隕∝書蟶�ｽ逧�ｨ｡譚ｿ�檎函謌仙勣蟆�ｼ壻ｽｿ逕ｨ螳�ｻｬ縲

```bash
php artisan generate:publish-templates
```

菴隕∝､榊宛謇譛荏app/templates`逶ｮ蠖穂ｸ狗噪讓｡譚ｿ縲ゆｽ蜿ｯ莉･菫ｮ謾ｹ霑吩ｺ帛宵隕∽ｽ貊｡諢丞ｮ�噪譬ｼ蠑上ょｦよ棡菴蝟懈ｬ｢荳榊酔逧�岼蠖包ｼ

```bash
php artisan generate:publish-templates --path=app/foo/bar/templates
```

蠖謎ｽ霑占｡形generate:publish-templates` ,螳�ｹ滉ｼ壼ｰ��鄂ｮ蜿大ｸ�芦`app/config/packages/way/generators/config/config.php`譁�ｻｶ縲りｿ吩ｸｪ譁�ｻｶ逵玖ｵｷ譚･譛臥せ蜒擾ｼ

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

蜷梧慮�悟ｽ謎ｽ菫ｮ謾ｹ霑吩ｸｪ譁�ｻｶ逧�慮蛟呻ｼ梧ｳｨ諢丈ｽ荵溷庄莉･譖ｴ譁ｰ豈丈ｸｪ鮟倩ｮ､逧�函謌仙勣逶ｮ譬�岼蠖輔

### Shortcuts 蠢ｫ謐ｷ蜻ｽ莉､

蝗荳ｺ菴蜿ｯ閭ｽ莨壻ｸ谺｡蜿井ｸ谺｡逧�醗蜈･螯ゆｸ句多莉､�悟多莉､蛻ｫ蜷肴仞辟ｶ譏ｯ譛画э荵臥噪縲

```bash
# Generator Stuff
alias g:m="php artisan generate:model"
alias g:c="php artisan generate:controller"
alias g:v="php artisan generate:view"
alias g:s="php artisan generate:seed"
alias g:mig="php artisan generate:migration"
alias g:r="php artisan generate:resource"
```
霑吩ｺ帛ｰ�｢ｫ菫晏ｭ假ｼ御ｾ句ｦゑｼ御ｽ逧Я~/.bash_profile` 謌冶 `~/.bashrc` 譁�ｻｶ荳ｭ縲




















