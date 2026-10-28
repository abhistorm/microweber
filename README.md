# Microweber: Drag-and-Drop CMS


## What is Microweber?


Microweber is a Drag-and-Drop website builder and a robust next-generation Content Management System (CMS) based on the PHP Laravel Framework. 
It empowers you to create various types of websites, online stores, and blogs without requiring any technical expertise.

At its core, Microweber is designed to support your journey toward online success. 
It offers an array of modules, customizations, and features tailored to e-commerce enthusiasts and bloggers. 
The CMS leverages the latest Drag & Drop technology and real-time text editing for an enhanced user experience, streamlined content management, visual appeal, and flexibility.

## Core Features of Microweber

### Drag & Drop

Microweber utilizes intuitive Drag & Drop technology, enabling users to manage content effortlessly by simply clicking and dragging elements across the screen. This functionality extends to various content types, including images, text fields, videos, and a variety of modules and customization options. The default template, "Dream," boasts over 75+ pre-designed layouts available for instant use via drag and drop.

### Real-Time Text Editing

Live Edit view is the embodiment of Microweber CMS's Real-Time Text Writing & Editing feature, allowing you to make changes to your website's interface in real time.


### Powerful Admin Panel

Microweber equips you with the capability to add dynamic pages, posts, and products, which can be organized into custom categories for enhanced navigation and content presentation. New pages can be created using different layouts, and each page, post, or product comes with a variety of preset layouts and modules to jumpstart your content creation. You can also add your custom modules to tailor your content precisely to your needs.

### E-commerce Solution

Microweber CMS primarily focuses on e-commerce, making it an ideal choice for aspiring online entrepreneurs. The software includes built-in features that support online shop founders, helping their businesses grow and excel.

## See it in action


## System Requirements

To run Microweber, you need the following components:

- HTTP server
- Database server
- PHP >= 8.2
    - `lib-xml` with DOM support
    - `GD` PHP extension
    - `intl` PHP extension
    - `curl` PHP extension
    - `json` PHP extension
    - `openssl` PHP extension
    - `sodium` PHP extension
    - `mbstring` PHP extension
    - `bcmath` PHP extension
    - `zip` PHP extension
    - `openssl` PHP extension
    - `bcmath` PHP extension
    - `fileinfo` PHP extension
    - `pdo_sqlite` PHP extension
    - `pdo_mysql` PHP extension

### PHP installation command

```bash
sudo apt install php8.2-{bcmath,bz2,curl,curl,dom,fileinfo,gd,intl,mbstring,mysql,opcache,sqlite3,xmlrpc,zip}
```


### HTTP Server

#### Apache

Ensure that the `mod_rewrite` module is enabled in your Apache configuration. Microweber automatically creates necessary `.htaccess` files during installation, including one with a `Deny All` directive in each folder to prevent unauthorized access to entry points other than `index.php`.

#### Nginx

For Nginx, add the following `location` directive to your server configuration block. The `root` directive should point to the base folder of your Microweber website (usually where this readme is located).

```nginx
server {
  location / {
    try_files $uri $uri/ /index.php$is_args$args;
  }
  location ~ /(vendor|src|config|database|bootstrap|storage|app|routes|.git|.env) {
    deny all;
    return 404;
  }
}
```

### IIS

You can import the `.htaccess` rewrite rules for IIS. Ensure that the URL Rewrite module is enabled for your website.

### Database

Microweber supports multiple database engines, including MySQL, SQLite, Microsoft SQL Server, and PostgreSQL. For small websites, SQLite is highly recommended. During installation, you can select from the databases enabled in your PHP configuration. If your preferred database server isn't listed, make sure to enable the corresponding PDO extension for your server in your PHP configuration.

## Installation


### Via Composer

#### Installing Dependencies


Install Microweber with `composer` command:

```bash
composer create-project microweber/microweber my_site dev-master  
```

Install NPM dependencies:

```bash
npm install
```
Build NPM dependencies:

```bash
npm run build
```

This command will install Microweber in a folder named `my_site`. Alternatively, you can clone the repository and then run `composer install` in the base directory.

#### File Permissions

Make sure that the following folders, and everything inside them, are writable by the user running the PHP scripts:

- config/
- storage/
- userfiles/
