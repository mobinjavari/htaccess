<div align="center">
  <h1>How to use htaccess</h1>
  <p>Hello, here we are going to teach you how to use htaccess</p><br><br>
  <div align="left">
    <ul>
      <li>Preventing the theft of files and folders on the host :</li><br>
      <pre><code>Options –Indexes
Options All -Indexes</code></pre><br>
      <li>Introducing the default language :</li><br>
      <pre><code>AddDefaultCharset UTF-8
DefaultLanguage fa-IR</code></pre><br>
       <li>Block Access to a Comprehensive Range of Files :</li><br>
      <pre><code>&lt;Files ".(htaccess | htpasswd | ini | phps | fla | psd | log | sh)$"&gt;
 Order Allow,Deny
 Deny from all
&lt;/Files&gt;</code></pre><br>
      <li>Return 404 if original request is .php :</li><br>
      <pre><code>RewriteCond %{THE_REQUEST} "^[^ ]* .*?\.php[? ].*$"
RewriteRule .* - [L,R=404]</code></pre><br>
      <li>Run Php without filename extension :</li><br>
      <pre><code>RewriteEngine on
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME}.php -f
RewriteRule ^(.*)$ $1.php</code></pre><br>
      <li>Redirect the browser to https :</li><br>
      <pre><code>RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]</code></pre><br>   
      <li>Setting custom pages on error pages :</li><br>
      <pre><code>ErrorDocument 401 /error/401.php
ErrorDocument 403 /error/403.php
ErrorDocument 404 /error/404.php
ErrorDocument 500 /error/500.php</code></pre>
      <li>Change the title and extension of the default index file when loading :</li><br>
      <pre><code>DirectoryIndex file.php file.html</code></pre><br>
      <li>Limit the type of executable files and display :</li><br>
      <pre><code>Options +FollowSymlinks
RewriteEngine On
rewritecond %{REQUEST_FILENAME} !^(.+).css$
rewritecond %{REQUEST_FILENAME} !^(.+).js$
rewritecond %{REQUEST_FILENAME} !file.php$
RewriteRule ^(.+)$ /deny/ [nc]</code></pre><br>
      <li>Creating restrictions on uploading files :</li><br>
      <pre><code>php_value upload_max_filesize 20M</code></pre><br>
      <li>Display request timed message in a specified time period :</li><br>
      <pre><code>php_value max_execution_time 200</code></pre><br>
      <li>Maximum time to receive POST and GET information :</li><br>
      <pre><code>php_value max_input_time 250</code></pre><br>   
    </ul>
  </div>
</div>
