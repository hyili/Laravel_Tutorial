# Laravel_Tutorial
For Laravel Tutorial Class Use

## Composer
### Create your first laravel project:
```
composer create-project laravel/laravel {project-name} --prefer-dist
```
* Descirption:
  * --prefer-dist is to using .zip file from github instead of using src code.

### Laravel-installer - a quicker laravel dependency manager:
* Composer is too slow ?? Using following command to install laravel-installer.
```
composer global require laravel/installer
```
* The command description is in:
```
laravel
```
* To create laravel project:
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
