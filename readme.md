# DT Demo Importer for WordPress themes
A One Click Demo Installer Class for WordPress Themes. This class developed for creating a quick installer for wordpress.


# Quick Usage

**Place this code in functions.php**
````php
/**
 * Initialize DT Importer
 */
$settings      = array(
  'menu_parent' => 'tools.php',
  'menu_title'  => __('Demo Importer', 'dt-importer'),
  'menu_type'   => 'add_submenu_page',
  'menu_slug'   => 'dt_demo_importer',
);
$options        = array(
    'demo-1' => array(
      'title'         => __('Demo 1', 'dt-importer'),
      'preview_url'   => 'https://www.google.com/',
      'front_page'    => 'Home',
      'blog_page'     => 'Blog',
      'menus'         => array(
            'primary'   => 'Primary', // Menu Location and Title
            'secondary' => 'Secondary',
        )
    ),
    'demo-2' => array(
      'title'         => __('Demo 2', 'dt-importer'),
      'preview_url'   => 'https://www.yahoo.com/',
      'front_page'    => 'Home',
      'blog_page'     => 'Blog',
      'menus'         => array(
            'primary'   => 'Primary',
            'secondary' => 'Secondary',
        )
    ),
    'demo-3' => array(
      'title'         => __('Demo 3', 'dt-importer'),
      'preview_url'   => 'https://www.google.com/',
      'front_page'    => 'Home',
      'blog_page'     => 'Blog',
      'menus'         => array(
            'primary'   => 'Primary',
            'secondary' => 'Secondary',
        )
    ),
);
DT_Demo_Importer::instance( $settings, $options );

````

**Create Folder by id in ````dt_importer/demos/```` by same id**
````php
demos
  - demo-1
    - content.xml // WP Exported Data
    - options.txt // Codestar Exported Options data
    - screenshot.php // Preview Image
  - demo-2
    - content.xml // WP Exported Data
    - options.txt // Codestart Exported Options data
    - screenshot.php // Preview Image
  - demo-3
    - content.xml // WP Exported Data
    - options.txt // Codestar Exported Options data
    - screenshot.php // Preview Image
````

Now go to the Tools >> Demo Importer :)

# Few screenshots
![Dashboard](http://i.imgur.com/u8oknuS.jpg)

# Under Development
* This class only import codestar settings only and planned to support others framework (Like: redux, option tree)
* Planned to support widget import.

# Credits
* [Codestar](https://github.com/Codestar/codestar-framework)
* [FrankM1](https://github.com/FrankM1/radium-one-click-demo-install)

# Licence
GPL V2+
