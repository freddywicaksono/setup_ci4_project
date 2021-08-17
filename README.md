# Setup CodeIgniter 4 Project in Windows using XAMPP
This tutorial give step by step to setup a new project for CodeIgniter 4

## Requirement
    php 7.3+
    extension=intl
    extension=mbstring
    extension=curl
    extension=mysqli
    
## 1. Download Codeigniter

    https://codeigniter.com/download

## 2. Extract file

  output:
  
    framework-4.x.x
    
## 3. Copy ci4 folder to xampp/htdocs and rename the folder

## 4. Open the folder in terminal as administrator

## 5. Add some library to project using composer
    
    composer install -vvv
    
## 6. Edit file: project_name/app/Config/App.php

    public $baseURL = 'http://localhost:8080';
    
 change to:
 
    public $baseURL = 'http://localhost/your_project_name/';

 and also:
 
    public $uriProtocol = 'REQUEST_URI';

 change to:
 
    public $uriProtocol = 'PATH_INFO';
    
## 7. copy index.php and .htaccess from public directory to root project folder

## 8. Edit index.php in root project folder

    $pathsConfig = FCPATH . '../app/Config/Paths.php';
    
 change to:
 
    $pathsConfig = FCPATH . 'app/Config/Paths.php';
    
## 9. Test on Browser

    http://localhost/[project_name]
