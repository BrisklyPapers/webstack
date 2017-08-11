# Briskly Papers

## About Briskly Papers
A fast and simple document store. Its goal is to provide a simple way to store and find all your documents.

## Getting started

`docker-compose up -d`

The new interface (under construction) is available at `http://localhost:3000/`

A working interface is available at `http://localhost:8085/`

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
