# Dockerize Rails app 

   * Dockerfile with base image, set workdir, copy gem files, copy main app, and expose port 3000

   * Docker build -t 'imagename' . 

   * Add .dockerignore to exclude files from container, similar to .gitignore

   * Create docker-compose.yml file with two containers, app and postgres
    * link app with postgres using 'links:'
    * pull image from dockerhub for postgres

   * Modify database.yml from sqlite to postgres
    * add ENV for postgres_port_5432_TCP_ADDR and PORT into yml
      * 'docker compose run app env' to print out list of environment variables

   * docker-compose build, docker-compose app rake db:create, and then docker-compose up to start up
