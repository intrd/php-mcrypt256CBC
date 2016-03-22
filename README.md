```
/**
 * php - Secure Encryption & Decryption Made Easy with PHP, MCrypt, Rijndael-256, and CBC
 * 
* @package php-mcrypt256CBC
* @version 1.0
* @category functions
* @author intrd - http://dann.com.br
* @see inspired by joshhartman http://www.warpconduit.net/2013/04/14/highly-secure-data-encryption-decryption-made-easy-with-php-mcrypt-rijndael-256-and-cbc/
* @copyright 2015 intrd
* @license http://creativecommons.org/licenses/by/4.0/
* @link https://github.com/intrd/php-mcrypt256CBC/
*/
```
## System installation
```
apt-get update & apt-get upgrade
apt-get install php5-curl php5-sqlite php5-cli

apt-get install git
git clone https://github.com/intrd/php-mcrypt256CBC/
```

## Usage sample
```
if (!defined('ENCRYPTION_KEY')) define('ENCRYPTION_KEY', "12345677378111147486847454344411"); //set your private key

$text="my test";
$text=mc_encrypt($text); //encrypt $text using defined privatekey
echo $text; //show encrypted text

$text=mc_decrypt($text); //decrypt $text using defined privatekey
echo $text; //show plaintext


```
