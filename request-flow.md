# Mammoth Request/Application Flow

 1. Public `index.php` is hit (any non existing file/directory is rewriten to `index.php` by Apache)
 1. The standard `index.php` checks if a `down` file[1], which if exists returns a `503` status code and maintenance page.
 1. The sites `include.php` is called.
 2. The environment is loaded...
   1. The local environment is loaded `local.php`
   2. The environment defined by the local environment (`define('ENVIRONMENT', 'development')`) loaded
   3. The global environment is loaded.
 2. The application is loaded...
 3. The modules are loaded...
 4. The application handles the request
   1. Module configuration is loaded [2]
   2. Application configuration is loaded [2]
   3. The router is iterated, each matching route returns a response.
     1. The application detects the repose, and if acceptably transmits it.
     2. Otherwise the application sends the corresponding HTTP code (typically 404). 
 4. 


[1] At this stage your can check for specific IP's allowed to bypass the maintenance page, and or secret query strings etc.

[2] Application and module configuration is cached in production environments.