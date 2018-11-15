# ClassicPress composer boilerplate

## Requirements

* PHP >= 5.3
* Composer - [Install](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx)

## Installation

1. Run in command line : `composer create-project --remove-vcs pierre-dargham/classicpress-composer-boilerplate my-project && cd my-project`
2. In wp-config.php, edit following constants : `DB_NAME`, `DB_USER`, `DB_PASSWORD`, `DB_HOST`, and `WP_HOME`
3. Run in command line : `composer install`
4. Create your database
5. Go to your site home url, and follow standard ClassicPress install steps

## Further steps

- If you are using a VCS, like git or svn, you may want to ignore thoses files :
```
- /vendor
- /wp
- /wp-content/themes/twentyseventeen
```
