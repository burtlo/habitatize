# Habitatize

"Habitatize Yourself" (tm) in this web application.

![Habitatize Meme](https://user-images.githubusercontent.com/244426/31551693-ec82d9fa-affa-11e7-8276-6b5c3cfb0483.gif)

## Building and Running with Habitat

1. Install [Habitat](https://www.habitat.sh/tutorials/download/)
2. Install [Docker](https://www.docker.com/get-docker)

3. Build the Habitat package and run it

```
$ export HAB_DOCKER_OPTS="-p 8000:8000"
$ hab studio enter
$ build
$ hab svc start YOURORG/habitatize
```

Visit the site in your browser at http://localhost:8000

4. Build the Habitat package and export it to Docker

```
$ hab studio enter
$ build
$ hab pkg export docker YOURORG/habitatize
$ exit
$ docker run -p 9000:9000 YOURORG/habitatize
```


## Building and Running with Ruby

1. Install Ruby.

There are a lot of ways that you can do it for your platform. I leave that information to better resources.

2. Install ImageMagick

Refer to the installing ImageMagick information below. I provide instructions for a few platforms.

3. Install Gems

    $ bundle install

4. Run

    $ rackup


## Install ImageMagick

Here are are some instructions for installing ImageMagick on a few platforms.

### CentOS

$ sudo yum install ImageMagick-devel ImageMagick-c++-devel

### Mac OSX

Install Homebrew (https://brew.sh/)

$ brew install pkg-config
$ brew install imagemagick@6 && brew link imagemagick@6 --force

### Windows

Install Chocolately (https://chocolatey.org/install)

$ choco install ruby
$ choco install imagemagick --version 6.9.9.9 -PackageParameters InstallDevelopmentHeaders=true
