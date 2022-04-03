# WordPress + Xdebug + Docker + Phpmyadmin in Visual Studio Code
I'm new to wordpress plugin so I was looking for away to develop and debug on the same time. Their where some god information on internet but no one with all components I was looking for. I start to try Laragon but then you need to install a lot on your local macine to get everything to work. So finally I find Docker, so the idea behind this repository is to schare my developement setup to simplify the start of the development with WordPress and of course, keep your machine clean.

This repository allows you to quickly start developing and/or debugging your WordPress theme or plugin.

## Requirements 😎
- Install Git
- Install Docker
- Install Visual Studio Code
- Install PHP
- Install Xdebug extension for Visual Studio Code
The code in this repository has been tested using Windows 10

These are the versions of the tools used:

Visual Studio Code: v1.65.2 | [download](https://code.visualstudio.com/download)
Xdebug extension for Visual Studio Code (PHP Debug): v1.13.0 | download
Docker Desktop: 2.0.0.3 (31259) | download
Docker compose: v3.7
Wordpress Image: wordpress:5.2.4-php7.3 | download
Xdebug: v2.6.1 | home page
Steps to use this repository 🤓
1. Clone the repository.

git clone https://github.com/fgarciachipi/wordpress-xdebug.git
git clone

Once the repository is cloned, we need to create a folder named html inside the repository folder. This folder is used for the WordPress container to storage the site (see docker-compose.yml file).

At this point you should have these folders in your local repository:

local folders

2. Run the container.

Inside the wordpress-xdebug folder run the following command:

docker-compose -f docker-compose.yml up
Wait until the command finishes and then access http://localhost:8080/, this is the url where the WordPress site is running.

3. Start coding.

After the container is running you can open the folder wordpress-xdebug in the Visual Studio Code and see that the folder html is not empty, it has the WordPress files.

VS

There is a launch.json file inside the folder .vscode with the debug configuration. Add the breakpoints in the code and go to the Debug Menu (Ctrl + Shift + D) and click on the Start Debugging button.

xdebug

Final notes ☕
Check that your Docker is configured to run linux container.
Since the html folder is excluded from git, if you are going to create a theme or a plugin you need to add the exception to the .gitignore file. (See line 26 for plugins and line 32 for themes)
