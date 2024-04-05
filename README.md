<h2 align="center">
  PHP_ATEC_Central_system_SQLMODI - v.1<br/>
  <a href="https://joezercardozaportfolio.web.app/" target="_blank">Cardoza, Joezer E.
  </a>
</h2>
<div align="center">
  <img alt="Demo" src="./images/LOGO.png" />
</div>

<br/>


This project was built using these technologies.

- PHP
- CSS
- JS
- SQL Server Management

## Features

**📖 Multi-Page Layout**

**🎨 Styled with React-Bootstrap and Css with easy to customize colors**

**📱 Fully Responsive**

## Getting Started

Clone down this repository. You will need `node.js` and `git` installed globally on your machine.

##Documentation

1. Installation - XAMPP
apachefriend.org

check phpinfo();

Microsoft Drivers for PHP for SQL Server
C:\xampp\htdocs - here is the code to modify
in visual studio code need to setup the file>preferences>settings>extenstions>php>edit in settings json

Installation PHP UAC problem

Regedit

Localmachine>software>Microsoft>windows>CurrentVersion>policies>system
Enable LUA - 0
----------------------------------------------------------------------------------------------------------------

2. Connect PHP to Mes_ATEC (Database)

----------------------------------------------------------------------------------------------------------------
1. check in my case PHP Version 8.2.12
<?php
phpinfo();
?>

2. go to github
https://github.com/microsoft/msphpsql/releases/
download 8.2 for windows 64bit

3. extract extensions
nts and ts dll

4. Drivers Installatio go to C:\xampp\php\ext
paste here 

5. Drivers Installation go to Xampp control panel apache>config>php ini
search curl
paste this code 
extension=php_pdo_sqlsrv_82_ts.dll
extension=php_sqlsrv_82_ts.dll
extension=php_pdo_sqlsrv_82_nts.dll
extension=php_sqlsrv_82_nts.dll

check the code


alternative check
Control Panel\System and Security\Administrative Tools
add sql and check logins

----------------------------------------------------------------------------------------------------------------
3. adding Logo in Tab HTML
add this code
Note: need to add the Image in the folder.

<link rel="icon" href="../images/LOGO.png" type="image/png">
----------------------------------------------------------------------------------------------------------------
4.the certificate chain was issued by an authority that is not trusted odbc driver 18 for sql server
NOTE if ito ang Issue

need to download --msodbcsql
https://go.microsoft.com/fwlink/?linkid=2249006
install it

kapag naman nakakapag query pero need ay kung trusted ba daw ito ang need gawin yung trusted
ServerCertificate need gawin = true
SQL handlerFor PHP
	function executeSQLQuery($sql, $params = array()) {
    // Database connection options
    $serverName = "MSDynamics-DB\AXDB"; // Server name
    $connectionOptions = array(
        "Database" => "CentralAccess", // Database name
        "Uid" => "sa",                 // Username
        "PWD" => "p@ssw0rd",        // Password
        "TrustServerCertificate" => true
    );
    
----------------------------------------------------------------------------------------------------------------

### Show your support

Give a ⭐ if you like this website!
