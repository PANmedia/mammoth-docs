# Application Flow (HTTP)

[Draft 2/26/2014 11:53:50 PM]

 1. Apache rewrite to `public/index.php`, or serve the file if it exists (images, css, etc).
 1. Check for `down` file (down for maintenance flag) and display maintenance file (`maintenance.php`) if applicable.
 1. Include the application bootstrap (`include.php`).
 1. Load the Composer autoloader.
 1. Load any files not autoloader compatible (i.e. function definitions). 
 1. Load the local environment files (***An error will occur if this does not exist***), then the global environment files. 
 1. Initialise, and return the application (to `public/index.php`).
 1. Dispatch the application [routes].

## Routing Flow

 1. Iterate ***all*** routes.
 1. Detect if there is a valid response (render, redirect, etc).
   - If there is no response, add an appropriate response. Typically a 404 not found render/header response.
 1. Process/output the response.