[![Latest Stable Version](https://poser.pugx.org/pierre-dargham/classicpress-composer-boilerplate/v/stable)](https://packagist.org/packages/pierre-dargham/classicpress-composer-boilerplate)
[![License](https://poser.pugx.org/pierre-dargham/classicpress-composer-boilerplate/license)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)

# ClassicPress composer boilerplate

This boilerplate shows the minimal steps required to start a composer project based on [ClassicPress](https://www.classicpress.net/).

Default dependencies are [ClassicPress core last release](https://github.com/ClassicPress/ClassicPress-release) and [Twenty Seventeen theme](https://wordpress.org/themes/twentyseventeen/).

## Requirements

* PHP >= 5.3
* [Composer](https://getcomposer.org/)

## Installation

1. Run in command line : `composer create-project --remove-vcs pierre-dargham/classicpress-composer-boilerplate my-project && cd my-project`
2. In wp-config.php, edit following constants : `DB_NAME`, `DB_USER`, `DB_PASSWORD`, `DB_HOST`, and `WP_HOME`
3. Run in command line : `composer install`
4. Create your database
5. Go to your site home url, and follow standard ClassicPress install steps

**Note:** Your site administration area will be available at `/classicpress/wp-admin/` instead of `/wp-admin/`

## Further steps

### Versionning

If you are using a VCS, like git or svn, you should ignore those files :
```
- /vendor
- /wp
- /wp-content/themes/twentyseventeen
```

### WordPress plugins and theme

You can install and manage WordPress plugins and theme using composer, thanks to composer miror repository [wpackagist](https://wpackagist.org/). If you require WordPress plugins and theme using composer, you should ignore them in your VCS also, like any other dependency.

### Automatic updates

Automatic updates are disabled by default in this boilerplate [wp-config.php](https://github.com/pierre-dargham/classicpress-composer-boilerplate/blob/master/wp-config.php), because you dependencies updates should be handled using Composer. If you need to change that, you can update the two following constants :
```
/* Automatic updates */
define('WP_AUTO_UPDATE_CORE', false);
define('AUTOMATIC_UPDATER_DISABLED', true);
```

### Nightly builds

If you want to install ClassicPress nightly builds instead of stable releases, you have to modify the `composer.json` file :

- Add `"minimum-stability" :"dev"`
- Add the following repository : `"type": "vcs", "url": "ssh://git@github.com/ClassyBot/ClassicPress-nightly.git"`

You should now have a section like that :
```
"minimum-stability" :"dev",
"repositories": [
    {
        "type": "composer",
        "url": "https://wpackagist.org"
    },
    {
        "type": "vcs",
        "url": "ssh://git@github.com/ClassyBot/ClassicPress-nightly.git"
    }
],
```

- Run `composer update classicpress/classicpress` to download the last nightly build

## Related links

- https://getcomposer.org/
- https://docs.classicpress.net/installing-classicpress/installing-with-composer/
- https://roots.io/using-composer-with-wordpress/
- https://composer.rarst.net/
