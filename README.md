<div align="center">
  <h1>Tips for using htaccess</h1>
  <p><a href="guide.md">Guide to using htaccess</a> / <a href=".htaccess">An example htaccess file</a></p><br><br>
  <div align="left">
    <ol>
      <li><strong>Authorization, Authentication</strong> : htaccess files are often used to specify the security restrictions for the particular directory, hence the filename "access". The htaccess file is often accompanied by an htpasswd file which stores valid usernames and their passwords.</li><br>
      <li><strong>Customized Error Responses</strong> : Changing the page that is shown when a server-side error occurs, for example HTTP 404 Not Found. Example : ErrorDocument 404 /notfound.html</li><br>
      <li><strong>Rewriting Urls</strong> : Servers often use htaccess to rewrite "ugly" URLs to shorter and prettier ones.</li><br>
      <li><strong>Cache Control</strong> : htaccess files allow a server to control User agent caching used by web browsers to reduce bandwidth usage, server load, and perceived lag.</li>
    </ol><br><br>
    <p>When a .htaccess file is placed in a directory which is in turn 'loaded via the Apache Web Server', then the .htaccess file is detected and executed by the Apache Web Server software.</p>
    <p>These .htaccess files can be used to alter the configuration of the Apache Web Server software to enable/disable additional functionality and features that the Apache Web Server software has to offer.</p>
    <p>These facilities include basic redirect functionality, for instance if a 404 file not found error occurs, or for more advanced functions such as content password protection or image hot link prevention.</p>
    <p>Whenever any request is sent to the server it always passes through .htaccess file. There are some rules are defined to instruct the working.</p><br>
  </div>
</div>
