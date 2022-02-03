# October CMS - Basic Auth Plugin

This plugin adds a Basic Auth to your CMS (Frontend/Backend) with configurable Username/Password.


## Configuration

Is directly in the backend -> settings.

Default credentials are admin/admin

## If you are using PHP FastCGI

If you are using PHP FastCGI, HTTP Basic authentication may not work correctly out of the box. The following lines should be added to your .htaccess file:

    RewriteCond %{HTTP:Authorization} ^(.+)$
    RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]
