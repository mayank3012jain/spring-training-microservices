# spring-training-microservices

This repository consists of multiple apps created using spring framework. This is used to demonstrate how to use spring, data persistance, rest apis, config server and eureka.

Following are the services and their description-

## Product-app
An app that adds product data to a sql database using spring. Refer to the following repository's commits to check the various implementations of the app.
TODO: Add link to product-app

## Reviews-app
An app that exposes rest endpoints for adding reviews for products. It communicates with product app by acting as a client.

## Config server
Used to store configs and locate then dynamically

## Eureka server
Used to make inter-service communication easier

## API gateway
