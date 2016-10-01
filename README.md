# Django development environment
**Django containerised development environment without the hassle.**

This projet uses [Docker](https://www.docker.com) and [Docker Compose](https://docs.docker.com/compose/) to create a **resuable development environment** for your [Django](https://www.djangoproject.com) based applications. This project provides a full abstration of the following steps:

*  Installation of required packages in a isolated environment build upon the official [Python 3 image.](https://hub.docker.com/_/python/)
*  Installation and configuration of a Postgresql database.

This project works on all system supported by Docker (Linux/Unix, Windows, OSX).


Here's the few steps you need to follow to set the things up!

*  Install  Docker and Docker Compose following the official documentation.

*  Add your project folder in the root of this repository so the arborescence looks something like this:

        django_dev_env/
                Dockerfile
                docker-compose.yml
                requirements/
                your_project_folder/
                        manage.py
                        ...


*  Replace the PROJECT_FOLDER_NAME occurrences in the Dockerfile by the name of your project folder.

*  Build and deploy your brand-new development environment by running the following command:

        docker-compose up

You can now access your application on [http://localhost:8080](http://localhost:8080)

The code  presents in your application folder is automatically mounted into the application container and the development server restarted when a change is made.

If you need other Python packages, add them to the requirements.txt and re-deploy.

Feel free to open an issue if you have any questions or suggestions.


