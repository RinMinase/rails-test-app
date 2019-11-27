<h1 align="center"> Rin Minase's Anime Database </h1>

<p align="center">
    <a href="https://www.ruby-lang.org/en/">
        <img alt="Ruby" src="https://img.shields.io/badge/Ruby-2.5.7-red?logo=ruby&style=for-the-badge">
    </a>
    <a href="https://rubyonrails.org/">
        <img alt="Rails" src="https://img.shields.io/badge/Rails-5.2.3-red?logo=rails&style=for-the-badge">
    </a>
</p>

## Introduction
_Add info here_

## Getting Started

### Running the project
1. If you are running Windows 10, [download](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe) and install `Docker for Windows`.

    **Note:** If you're not running Windows 10, use `Docker Toolbox` instead, [download](https://docs.docker.com/toolbox/toolbox_install_windows/#step-2-install-docker-toolbox) and install it. Also make sure that you are also running [vitualization](https://docs.docker.com/toolbox/toolbox_install_windows/#step-1-check-your-version).

2. Clone the project

    ```
    git clone https://github.com/RinMinase/rails-test-app.git
    cd rails-test-app
    ```

3. Build the necessary docker containers

    ```
    docker-compose run web rails new . --force --no-deps --database=postgresql
    docker-compose build
    ```

3. Run the created docker containers

    ```
    docker-compose up -d
    docker-compose run web rake db:create
    ```

4. Fire up your browser and go to `localhost:3000`.

    **Note:** If you are using `Docker Toolbox` instead of `Docker`, go to `192.168.99.100:3000` instead.

**Note:**
In case you need to remove the images
From the project folder, run:
1. `docker-compose down`
2. `docker images`
3. Look for the IDs of `rails-test-app_web_1`, `rails-test-app_db_1`
4. Run `docker rmi <Image ID> <Image ID>...`

### Re-running the project
1. Make sure `Docker` is running, then open your terminal.

    **Note:** If you are running `Docker Toolbox`, then open the docker terminal.

2. Navigate to the project foler then run `docker-compose up -d`

3. Fire up your browser and go to `localhost:3000`.

    **Note:** If you are using `Docker Toolbox` instead of `Docker`, go to `192.168.99.100:3000` instead.

### Project Structure
    .
    ├── ...                                 # Template
    └── ...                                 # Template

### Testing the project
_Add info here_

## Built with
* <img width=20 height=20 src="https://guides.rubyonrails.org/images/favicon.ico"> [Rails 5.2](hhttps://rubyonrails.org/) - Web Framework
* <img width=20 height=20 src="https://www.ruby-lang.org/favicon.ico"> [Ruby 2.5](https://www.ruby-lang.org/) - Language syntax
* <img width=20 height=20 src="https://www.postgresql.org/favicon.ico"> [PostgreSQL](https://www.postgresql.org/) - Database
* <img width=20 height=20 src="https://www.docker.com/sites/default/files/d8/Docker-R-Logo-08-2018-Monochomatic-RGB_Moby-x1.png"> [Docker](https://www.docker.com/) - Container platform

## Deployed to
