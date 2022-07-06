# Vaccination Service for Digital Village

This is a web app deployed on Microsoft Azure that provides an easy vaccination management service for the village administration as part of the village digitization super-project.

## About
Digital Village, as the name suggests is a project which aims to digitize most(if not all) of
village’s records, information communication and daily functioning. To achieve this, we shall
build a Mobile App. The app will be capable of hosting and notifying the members with village
related news, relevant government schemes and current affairs, providing personal portals to store
data like bills, payments, etc. In the current scenario, this will track, edit, update etc the Covid
Vaccination details of every member in the village. Additionally analysis updates related to the
current activity, say spread of the new Covid variant shall be published so as to also work as a
holistic local news medium. This way, the app shall serve the purpose of an all-in-one platform
customized to suit the needs of the rural community in an area.

1. application website through netlify: https://vaxmodule.netlify.app/ or http://vax-module-frontend.azurewebsites.net/

2. backend running with azure: https://vax-module-2.azurewebsites.net/

3. database hosted with azure: vax-module-db.postgres.database.azure.com

>Following is an end-to-end stepwise guide to create amd integrate all the parts of the software

# 1. Django App

## Install Virtualenv
To install virtualenv, use the pip package manager that comes pre-installed with Python. Use the following command on the command prompt. You can access the command prompt by simply search for cmd on your Start menu. Then, click to open.

`pip install virtualenv`

After successful installation, virtualenv should now be in the Scripts folder inside the Python installation folder on your local disk.

Locate where Python is installed on your PC
While installing a Python software distribution on your PC, if you selected the option to _ADD PYTHON TO PATH_, then you would find its location in the _PATH_ variable.

Otherwise, you will have to look into your local disk to check for its path. The location would be in a path that looks like the following:

`C:\Users\%username%\AppData\Local\Programs\Python\Python37\python.exe`

Therefore, you need to find python.exe in the location that looks like the above and take a note of it. Now, we shall create a virtual environment for our project

Create a virtual Python Environment for your Project
To create a virtual environment for you, change directory to the place where you want your Django project to be. Use the cd command on your command prompt to move to the said directory as follows:

`cd backend`

Now, you should use the virtualenv command appended with --python to create a new Python environment for your project. You also need to have the Python installation path that you noted from Step 2 above in the same line of command. Then finish off with a name for your new virtual environment, we can call it env for example. See the following:

`virtualenv --python C:\Path\To\Python\python.exe env`

## Activate the Virtual Environment

At this point, you need to activate the virtual environment for you to be able to work in it. Activate it by:

`.\venv\Scripts\activate`

So, your command line will change to show the activate environment name like the following:

`(env) C:\Users\%username%\Path\To\Project\Directory`

Nice! Now, you can create your Django project and do any other thing that you want active inside the virtual environment.

However, you can deactivate when you are done working or want to leave the virtual environment. Do it this way:

`deactivate`

Now, let’s go forward into creating a Django project in the new virtual environment.

## Create a Django Project
Firstly, install Django here. The installed Django package will only be active in this virtual environment and no other place on your PC.

`pip install Django`

You can check installed packages by creating a requirements.txt file. This file contains a list of all the installed packages and their respective versions.

`pip freeze > requirements.txt`

Now, you can create a Django project. Let’s call our project myproject for example:

`django-admin startproject VaxProject`

## Starting the API app

change the directory to this newly created project and execute the following command:

`python manage.py startapp api`

Now create the required files

## Setting up database

We've used [PostgreSQL](https://www.postgresql.org/download/), the settings for which have been made in the _settings.py_ file

# 2. React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

# 3. Deployment

We've followed the follwowing official microsoft tutorials to deploy the Vaccination module app to Azure platform

1. [Hosting Django App](https://www.youtube.com/watch?v=D6Wyk9q2JM0&t=9s)
2. [Adding Postgres Server](https://www.youtube.com/watch?v=Z4gLolNTM5I)
3. [Hosting React App](https://www.youtube.com/watch?v=Ny5vJRfQito)
