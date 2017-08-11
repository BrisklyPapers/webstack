# Briskly Papers

## About Briskly Papers
A fast and simple document store. Its goal is to provide a simple way to store and find all your documents.

## Getting started

`git submodule init`

start the docker stack

`$ docker-compose up -d`

### init app (laravel)

set environment variables

`$ cp ./php/src/.env.development ./php/src/.env`

install composer dependencies

`$ docker-compose exec app bash`

`root@aef84695e027:/var/www# composer install`

## take a look around

The new interface is available at `http://localhost:3000/`

## Environment

* Web Node (localhost:8085, container name: web), contains Nginx, connects to Laravel App
* App Node (container name: app), contains Laravel, provides all backend features
* Elasticsearch (localhost:9200, container name: elasticsearch1, elasticsearch2), contains all documents
* NodeJs - React (container_name: react), contains web frontend

## Directory structure



## System Requirements

* Docker
* For elasticsearch:
  * `sudo sysctl -w vm.max_map_count=262144`

## Troubleshooting

If http://localhost:8085/ is not responding as expected, there might be permission problems. Current workaround: `$ sudo chmod a+rwx -R ./php`

## Development

Working with git submodules: [git-scm](https://git-scm.com/book/en/v2/Git-Tools-Submodules)