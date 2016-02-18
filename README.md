# Laravel_Tutorial
* For Laravel Tutorial Class Use

## Composer
* a php framework package dependency manager.

### Create your first Laravel project:
```
composer create-project laravel/laravel {project-name} --prefer-dist
```
* Descirption:
 * --prefer-dist is to using .zip file from github instead of using src code.

### Laravel-installer - a quicker Laravel package dependency manager:
* Composer is too slow ?? Using following command to install laravel-installer.
```
composer global require laravel/installer
```
* The command description is in:
```
laravel
```
* To create Laravel project:
```
laravel new {project-name}
```

### Take over other project:
* Because there is usually no vendor/ and .env file when you download the other's project, so we could use the following command:
```
cd {project-name}
composer install --no-scripts
composer run-script post-root-package-install
composer run-script post-install-cmd
composer run-script post-create-project-cmd
```
* Description:
 * 1st one is to enter the preject dir.
 * 2nd one is to install the vendor/ from composer.json.
 * 3rd one is to create .env from .env.example.
 * 4th one is to optimized class.
 * 5th one is to generate the key.

## Package
### How to find a package?
* Website:
 * Packalyst: http://packalyst.com (only for Laravel framework)
 * Packagist: https://packagist.org (for php framework)
 * Packagist Semver Checker: http://semver.mwl.be
* Semantic versioning:
 * X.Y.Z
  * X: version: API change
  * Y: feature: New function
  * Z: patch: Fix bug
  * ex. 0.1.0 -> 0.1.1 -> 0.1.2 -> 1.0.0 -> 1.1.0 ...
* PSR
 * Auto-loader
 * PSR-4: current version
* Update rate, Author, Documentation, Popularity, etc.

### Composer.json
* To install a new package, add the following to composer.json.
```
"{developer}/{package-name}": "{version}"
```
* Check that the composer.json is valid.
```
composer validate
```
* Update the installed package.
```
composer update
```

### Config
* Add the package into Laravel. Open config/app.php file.
```
{developer}/{package-name}/ServiceProvider::class,
```
* Publish the config file, then you can edit it in the future.
```
artisan vendor:publish --provider="{developer}/{package-name}/ServiceProvider"
```

## Development
### Process
* Local machine -> Development machine -> Staging machine -> Production machine

### Environment
* .env and .env.example file, using following command can check the setting
```
artisan env
```
* Description:
 * .env file is the file that would be read by Laravel when running.
 * .env.example file is used to tell the developer to follow to assign the variable.

### Debug mode
* Open the .env file, this will show the debug message to the website.
```
APP_DEBUG=true
```
