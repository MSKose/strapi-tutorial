<h1 align="center">Strapi Tutorial</h1>

## Table of Contents

- [Overview](#overview)
- [Stack & Tools](#stack)
- [How to use](#how-to-use)

## Overview

This is my second attempt to create an api. With this tutorial, I saw the difference between the built-in api handling with Django and the 3rd party DRF way. I learned about the generic DRF views and saw how relatively easy it is to use compared to function based api handling.

![screenshot](./drf-tutorial-2.png)

<h2 id="stack">Stack & Tools</h2>

- Strapi
- Postman

## How To Use

```
# Clone this repository
$ git clone https://github.com/MSKose/strapi-tutorial.git

# Running this repo
    $ yarn install
    $ yarn develop
```

## populating endpoints that do not come by default
```
    $ baseUrl/api/appName?populate=fieldName
    or to get all the fields:
    $ baseUrl/api/appName?populate=*
```
## Acknowledgements
- Tutorial source: [Laith Academy](https://www.youtube.com/watch?v=vcopLqUq594&t=10s)
