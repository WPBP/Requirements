## WP Requirements 
[![License](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)
![Downloads](https://img.shields.io/packagist/dt/wpbp/requirements.svg) 

A small library to easily handle detection of minimum system requirements in WordPress plugins.

![Screenshot][1]

# Features

* Detects PHP versions incompatible with your Plugin.
* Detects WordPress versions incompatible with your Plugin.
* Detects WordPress plugins.
* Detects absence of PHP extensions.
* Displays errors to users without activating your Plugin.

# Getting Started

```php
new Plugin_Requirements( self::$plugin_name, self::$plugin_slug, array(
  'PHP' => new PHP_Requirement( '5.9.0' ),
  'WP' => new WordPress_Requirement( '3.9.0' ),
  'Extension' => new PHP_Extension_Requirement( array('mysql', 'mysqli', 'session', 'pcre','json', 'gd', 'mbstring', 'zlib' ),
  'Plugin' => new Plugin_Requirement( array( 
     array( 'Plugin not installed', 'slug/slug.php' ) , 
     array( 'Plugin not installed 2', 'slug/slug2.php' ) 
   ) )
) );
```

## License

Fork of Mte90, Copyright © 2014 Darshan Sawardekar

[1]: http://i.imgur.com/0d9d6HF.png
