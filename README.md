# php7-custom-router
Simple, fast custom PHP router

1) Place all files (index.php & the views folder) into the localhost root directory
2) Create a .htaccess file and place it in the root folder. The .htaccess file will have the following code:<br>
RewriteEngine On<br>
RewriteBase /<br>
RewriteCond %{REQUEST_FILENAME} !-d<br>
RewriteCond %{REQUEST_FILENAME} !-f<br>
RewriteRule ^(.+)$ index.php [QSA,L]`

3) Navigate to localhost (or localhost/) for the main route, localhost/about for the about route, and localhost/[insert_random_string] for the 404 (page not found) route
