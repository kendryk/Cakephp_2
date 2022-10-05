# Cakephp_2
Crétaion d'un site web sous cakephp


Tout d'abord, nous devons créer le répertoire du projet :

```
mkdir Cakephp_2 && cd Cakephp_2
```

Maintenant, la commande ci-dessous va créer un fichier **composer.json** avec **cakephp** comme dépendance. Le **–no-update** l'empêchera d'installer les dépendances dans le répertoire par défaut :

```
composer require --no-update cakephp/cakephp:2.10.*
```

Définissez le répertoire de dépendance sur **Vendor** :

```
composer config vendor-dir Vendor/
```

Et installez les dépendances

```
composer install
```

Générez le squelette de l'application :

```
Vendor/bin/cake bake project . --empty
```


Vous devez avoir ce meesage dans la ligne de commande
```
Welcome to CakePHP v2.10.17 Console
---------------------------------------------------------------
App : cakephp-app
Path: /Users/onoblog/codes/cakephp-app/
---------------------------------------------------------------
Skel Directory: /Users/onoblog/codes/cakephp-app/Vendor/cakephp/cakephp/lib/Cake/Console/Templates/skel
Will be copied to: /Users/onoblog/codes/cakephp-app/.
---------------------------------------------------------------
Look okay? (y/n/q)
```

Et entrez simplement **y** lorsque vous y êtes invité.

```
---------------------------------------------------------------
Created: app in /Users/onoblog/codes/cakephp-app/.
---------------------------------------------------------------
 * Random hash key created for 'Security.salt'
 * Random seed created for 'Security.cipherSeed'
 * Cache prefix set
 * app/Console/cake.php path set.
CakePHP is not on your `include_path`, CAKE_CORE_INCLUDE_PATH will be hard coded.
You can fix this by adding CakePHP to your `include_path`.
 * CAKE_CORE_INCLUDE_PATH set to /Users/onoblog/codes/cakephp-app/Vendor/cakephp/cakephp/lib in webroot/index.php
 * CAKE_CORE_INCLUDE_PATH set to /Users/onoblog/codes/cakephp-app/Vendor/cakephp/cakephp/lib in webroot/test.php
   * Remember to check these values after moving to production server
Project baked successfully!
```

N'oubliez pas de créer le fichier de configuration de la base de données !

```
cp Config/database.php.default Config/database.php
```

Et c'est tout! Il ne vous reste plus qu'à mettre à jour la configuration de la base de données avec les informations d'identification valides de la base de données.

Et aussi, si vous utilisez un gestionnaire de version comme **Git** , n'oubliez pas d'ignorer le  répertoire **Vendor** et  **tmp**  .
