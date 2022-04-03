# WordPress + Xdebug + Docker + phpMyAdmin in Visual Studio Code
I'm new to wordpress plugin so I was looking for away to develop and debug on the same time. Their where some god information on internet but no one with all components I was looking for. I start to try Laragon but then you need to install a lot on your local macine to get everything to work. So finally I chosed Docker Composer, beacause you can set up the enviroment by one file and keep your machine clean.

This repository allows you to quickly start developing and/or debugging your WordPress theme or plugin. The code in this repository has been tested using Windows 10

These are the versions of the tools used:

- Visual Studio Code: v1.65.2 | [download](https://code.visualstudio.com/download)
- Xdebug extension for Visual Studio Code (PHP Debug)
- Docker Desktop: 4.5.0 | [download](https://docs.docker.com/desktop/windows/install/)
- Wordpress Image: andreccosta/wordpress-xdebug
- PHP: v8.14 | [download](https://www.php.net/downloads)

## Requirements 😎
1. Install Git
2. Install Docker
3. Install PHP
4. Install Visual Studio Code
Set path to your php.exe in Visual Studio code settings.json
``` 
php.validate.executablePath 
php.debug.executablePath
```

5. Install Xdebug extension for Visual Studio Code

## Steps to use this repository 🤓
1. Clone the repository.

git clone https://github.com/eacydev/wordpress_docker_xdebug.git

Once the repository is cloned, we need to create two folders named wp and db_data inside the repository folder. The wp folder is used for the WordPress container to storage the site (see docker-compose.yml file) and the db_data folder is for MySql container to storage database data.

At this point you should have these folders in your local repository:
.vscode
db_data
wp

2. Run the container.

Inside the wordpress-xdebug folder run the following command:

docker-compose up -d
Wait until the command finishes and then access http://localhost:8080/, this is the url where the WordPress site is running.

3. Start coding.

After the container is running you can open the folder wordpress-xdebug in the Visual Studio Code and see that the folder wp is not empty, it has the WordPress files.

## To debug

There is a launch.json file inside the folder .vscode with the debug configuration. Add the breakpoints in the code and go to the Debug Menu (Ctrl + Shift + D) and click on the Start Debugging button.


## Final notes ☕
Check that your Docker is configured to run linux container.
