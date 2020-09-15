# LonellyMVC
A simple PHP MVC framework built only on php + PDO for Database class

# Files

Project file tree :
```
lonellymvc
├── app
│   ├── bootstrap.php
│   ├── config
│   │   └── config.php
│   ├── controllers
│   │   └── Pages.class.php
│   ├── helpers
│   ├── libraries
│   │   ├── Controller.class.php
│   │   ├── Core.class.php
│   │   └── Database.class.php
│   ├── models
│   └── views
│       ├── 404.html
│       ├── include
│       │   ├── footer.php
│       │   └── header.php
│       └── pages
│           ├── about.php
│           └── index.php
├── public
│   ├── css
│   │   └── main.css
│   ├── index.php
│   └── js
│       └── main.js
└── README.md
```

public folder is the main UI where user only have access
app is blocked by .htacces file and contins core functionallity (config, controllers, libraries, models, views).

### Config
Config file - site config + db credentials.
```PHP
// DB Params
define('DB_HOST', '_YOUR_HOST_');
define('DB_USER', '_YOUR_USER_');
define('DB_PASS', '_YOUR_PASSWORD');
define('DB_NAME', '_YOUR_DB_NAME_');

// App Root
define('APPROOT', dirname(dirname(__FILE__)));

// URL Root
define('URLROOT', 'http://lonellymvc.md/');

// Site Name
define('SITENAME', '_YOUR_SITENAME_');
```

### Controllers
Folder for site controllers, for example page controller for index html

#### Page
```PHP
public  function  index() // Shows index.php of the site

public  function  about() // Shows about page
```

### Libraries
Here is the core of the MVC, base classes defined
#### Controller Class
``` PHP
public  function  model($model) // Searchs and return a Model

public  function  view($view, $data = []) // Shows view and pass data
```

#### Core class
```PHP
protected  $_currentController = 'Pages';
protected  $_currentMethod = 'index';
protected  $_params = [];

public  function  __construct() // Setup controller and call methods

public  function  getUrl() // Return an array from url url:/controller/method/args
```

#### Database class
```PHP
private  $_host = DB_HOST;
private  $_user = DB_USER;
private  $_pass = DB_PASS;
private  $_db_name = DB_NAME;

private  $_dbh;
private  $_stmt;
private  $_error;

public  function  __construct()

// Prepare statment with query
public  function  query($sql)

// Bind values
public  function  bind($param, $value, $type = null)

// Execute prepare statment
public  function  execute()

// Get results as an array of objects
public  function  resultSet()

// Get a single row
public  function  single()

// Get row count
public  function  rowCount()

```
### Views
Main UI which will be compiled and shown to user.

# About author
## Student şi Part-Time worker
- 🔭 Studying deep web
- 🌱 I'm  constantly growing
- 👯 Open for new jobs
- 🥅 2020 Goals: Learn more about Web Development
- ⚡ Fun fact: I'm using vim (old-fag)

### Connect with me:

[<img align="left" alt="MrLonelly | Twitter" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/twitter.svg" />][twitter]
[<img align="left" alt="MrLonelly | LinkedIn" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />][linkedin]
[<img align="left" alt="MrLonelly | Instagram" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/instagram.svg" />][instagram]

[twitter]: https://twitter.com/mr_l0n3lly
[instagram]: https://www.instagram.com/apavalac/
[linkedin]: https://www.linkedin.com/in/andrei-pavalachi-270b3a167/
