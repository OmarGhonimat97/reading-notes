# Readings: Django REST Framework & Docker

## Beginner’s Guide to Docker

Docker is a way to isolate and run entire applications.

### Linux Containers

Docker is really just Linux containers which are a type of virtualization.

This, fundamentally, is what Docker is. A way to implement Linux containers!

An analogy we can use here is that of homes and apartments. Virtual Machines are like homes: stand-alone buildings with their own infrastructure including plumbing and heating, as well as a kitchen, bathrooms, bedrooms, and so on. Docker containers are like apartments: they share common infrastructure like plumbing and heating, but come in various sizes that match the exact needs of an owner.

### Containers vs Virtual Environments

### Conclusion

- Docker is a way to run Linux containers
- Containers are a lightweight alternative to Virtual Machines
- ***Dockerfile*** is a list of instructions for creating an image
- Images are made up of one or more layers
- Containers are a running instance of an image
- ***docker-compose.yml*** controls how to run the container
- Containers are stateless and ephemeral in nature. We can link the local filesystem via ***volumes*** but things become more complex with databases.


## Django for APIs - Library Website

Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework. It always must be added to a project after Django itself has been installed and configured.

### Traditional Django

A traditional Django website consists of a single project with multiple apps representing discrete functionality. 

> First app
> Models
> Admin
> Views
> URLs
> Templates
> Tests
> Git