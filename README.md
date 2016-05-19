<!-- docbloc -->
<span id='docbloc'>
PHP - Secure Encryption & Decryption Made Easy with PHP, MCrypt, Rijndael-256, and CBC
<table>
<tr>
<th>Package</th>
<td>intrd/php-mcrypt256cbc</td>
</tr>
<tr>
<th>Version</th>
<td>1.0</td>
</tr>
<tr>
<th>Tags</th>
<td>php, encryption, mcrypt, 256bits, cbc, rijndael</td>
</tr>
<tr>
<th>Project URL</th>
<td>http://github.com/intrd/php-mcrypt256cbc</td>
</tr>
<tr>
<th>Author</th>
<td>intrd (Danilo Salles) - http://dann.com.br
<tr>
<th>Author</th>
<td>Originally developed by Joshhartman - http://www.warpconduit.net/2013/04/14/highly-secure-data-encryption-decryption-made-easy-with-php-mcrypt-rijndael-256-and-cbc/</td>
<tr>
<th>Copyright</th>
<td>(CC-BY-SA-4.0) 2016, intrd</td>
</tr>
<tr>
<th>License</th>
<td><a href='http://creativecommons.org/licenses/by-sa/4.0'>Creative Commons Attribution-ShareAlike 4.0</a></td>
</tr>
<tr>
<th>Dependencies</th>
<td> &#8226; php >=5.3.0</td>
</tr>
</table>
</span>
<!-- @docbloc 1.1 -->

## System & Composer installation
```
$ sudo apt-get update & apt-get upgrade
$ sudo apt-get install curl php-curl php-cli php-mcrypt
$ curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
```

## Usage sample

Assuming your project are running over `Composer` PSR-4 defaults, simply Require it on your `composer.json`
```
"require": {
    "intrd/php-mcrypt256cbc": ">=1.0.x-dev <dev-master"
}
```
And run..
```
$ composer install -o #to install
$ composer update -o #to update
```
Always use -o to rebuild autoload.

Now Composer Autoload will instance the class and you are able to use by this way..

```
require __DIR__ . '/vendor/autoload.php';
use php\mcrypt256cbc as cry;

if (!defined('ENCRYPTION_KEY')) define('ENCRYPTION_KEY', "12345677378111147486847454344411"); //set your private key

$test="yeah it works!";
$text=cry::mc_encrypt($text,ENCRYPTION_KEY); //encrypt $text using defined privatekey
echo $text; //show encrypted text

$text=cry::mc_decrypt($text,ENCRYPTION_KEY); //decrypt $text using defined privatekey
echo $text; //show plaintext
```
