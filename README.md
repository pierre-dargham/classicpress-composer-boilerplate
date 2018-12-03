# ClassicPress composer boilerplate

This boilerplate shows the minimal steps required to start a composer project based on [ClassicPress](https://www.classicpress.net/).

Default dependencies are [ClassicPress core last release](https://github.com/ClassicPress/ClassicPress-release) and [Twenty Seventeen theme](https://wordpress.org/themes/twentyseventeen/).

## Requirements

* PHP >= 5.3
* [Composer](https://getcomposer.org/)

## Installation

1. Run in command line : `git clone git@github.com:pierre-dargham/classicpress-composer-boilerplate.git my-project && cd my-project && rm -rf .git`
2. In wp-config.php, edit following constants : `DB_NAME`, `DB_USER`, `DB_PASSWORD`, `DB_HOST`, and `WP_HOME`
3. Run in command line : `composer install`
4. Create your database
5. Go to your site home url, and follow standard ClassicPress install steps

## Further steps

- If you are using a VCS, like git or svn, you should ignore those files :
```
- /vendor
- /wp
- /wp-content/themes/twentyseventeen
```

## WordPress plugins and theme

- You can install and manage WordPress plugins and theme using composer, thanks to composer miror repository [wpackagist](https://wpackagist.org/).
- If you require WordPress plugins and theme using composer, you should ignore them in your VCS, like any other dependency.
