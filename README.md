# PHP File Manager

A good solution for managing files and folders on your site.

![PHP File Manager](https://raw.github.com/alexantr/filemanager/master/phpfm.png)

## How to use

Download ZIP with latest version from master branch.

Copy **filemanager.php** to your website folder and open it with web browser
(e.g. http://yoursite/any_path/filemanager.php).

Default username/password: **fm_admin**/**fm_admin**

*Warning:* Please set your own username and password in ```$auth_users``` before use.

To enable/disable authentication set ```$use_auth``` to ```true``` or ```false```.

You can include file manager in another scripts. Just define `FM_EMBED` and other necessary variables. Example:

```php
class SomeController
{
    public function actionIndex()
    {
        define('FM_EMBED', true);
        define('FM_LANG', 'en');
        define('FM_SELF_URL', UrlHelper::currentUrl());
        define('FM_SHOW_HIDDEN', false);
        require 'path/to/filemanager.php';
    }
}
```

Supports variables `FM_LANG`, `FM_ROOT_PATH`, `FM_ROOT_URL`, `FM_SELF_URL`, `FM_SHOW_HIDDEN`.

## Localization

To change default language set ```$lang``` value to one of supported languages in list below.

* English (en)
* Russian (ru)
* French (fr) - by [Nicolas Karolak](https://github.com/nikaro)

You can create file `filemanager-l10n.php` in folder with File Manager and put your own translations in it.
They will be merged with built-in translations.

## Bug tracker

If you have any issues with file manager, you may report them on
[Issue tracker](https://github.com/alexantr/filemanager/issues).

## License

This software is released under the MIT license.

Icons by [Yusuke Kamiyamane](http://p.yusukekamiyamane.com/).
