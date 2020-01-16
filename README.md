# Magento 2 Repository Example

This Magento 2 Repository Example is a starting point of all Magento 2 custom projects. It contains only necessary files, the files which are required for creating and extracting Magento 2 project on a server or a local environment.

It only includes 3 required files: 
* `.gitignore`
* `composer.json`
* `composer.lock`

In addition to this, if running with Apache2 server, .htaccess files are also included into the repository.
It can be necessary for the Content Delivery Network (CDN) custom configuration or PHP settings modifications, for example `memory_limit`.
* `pub/.htaccess`
* `pub/media/.htaccess`
* `pub/static/.htaccess`

That's it!

## The .gitignore file
The `.gitignore` file is modified in order to eliminate all unnecessary files from the repository.
Here are additional changes for the `.gitignore` file:
Copy these lines to your Magento 2 project's `.gitignore` file.
```
/.modman/
/app/*
/bin/*
/dev/*
/bin/*
/lib/*
/phpserver/*
/setup/*
/update/*
/.github/*
/pub/.user.ini
/pub/cron.php
/pub/get.php
/pub/health_check.php
/pub/index.php
/pub/static.php
/pub/opt/magento/var/resource_config.json
/pub/errors/*
/.htaccess
/.htaccess.sample
/.php_cs.dist
/.travis.yml
/.user.ini
/auth.json.sample
/CHANGELOG.md
/COPYING.txt
/grunt-config.json.sample
/Gruntfile.js.sample
/index.php
/LICENSE.txt
/LICENSE_AFL.txt
/nginx.conf.sample
/package.json.sample
/php.ini.sample
```

Also, there are some modifications in the `.gitignore` file for existing lines, please see [commit](https://github.com/pronkoconsulting/magento-2-repository-example/commit/94805111ab61bb83742cdd6be3bd97f5c8d838b4) for a better understanding.
Or simply add the following lines at the end of the `.gitignore` file.
```
#!/pub/media/attribute/.htaccess
#!/pub/media/catalog/.htaccess
#!/pub/media/customer/.htaccess
#!/pub/media/downloadable/.htaccess
#!/pub/media/import/.htaccess
#!/pub/media/theme_customization/.htaccess
#!/pub/media/wysiwyg/.htaccess
#!/pub/media/tmp/.htaccess
#!/var/.htaccess
#!/vendor/.htaccess
#!/generated/.htaccess
```

## How To Install
- check all the php extension are installed with running php version (check here)[https://magento.stackexchange.com/questions/123246/magento-2-php-extensions-missing]

- Download vendor packages using $composer update
  - provide the auth keys from magento marketplace and save in local in auth.json
- change the permission of directory with chmod and chown
- Now Install magento using (Commandline)[https://www.simicart.com/blog/magento-2-composer/] or BrowserSide
 
