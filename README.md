<h1 align="center">Strapi Tutorial</h1>

## Table of Contents

- [Overview](#overview)
- [Stack & Tools](#stack)
- [How to use](#how-to-use)

## Overview

This is my second attempt to create an api. With this tutorial, I saw the difference between the built-in api handling with Django and the 3rd party DRF way. I learned about the generic DRF views and saw how relatively easy it is to use compared to function based api handling.

<!-- ![screenshot](./drf-tutorial-2.png) -->

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

## Populating endpoints that do not get requested by default
```
    baseUrl/api/appName?populate=fieldName
```
### or to get all the fields:
```
    baseUrl/api/appName?populate=*
```

## Getting specific fields
### The default value is:
```
    baseUrl/api/appName?fields=*
```

### Filtering fields so we only get name field from appName:
```
    baseUrl/api/appName?fields=name
```
    
### Filtering and populating so we only get name and image:
```
    baseUrl/api/appName?fields=name&populate=image
```

## Sorting
### The following will get you names in ascending order
```
    baseUrl/api/appName?fields=Name&sort=Name
```
### To get it in descending order you add :desc as such:
```
    baseUrl/api/appName?fields=Name&sort=Name:desc
```
### Add another sorting parameter to have it sorted by that parameter if the first collides:
Note: Therefore, in the below example if there are two names that are same, sorting between them will depend on createdAt field
```
    baseUrl/api/appName?fields=Name&sort=Name:desc,createdAt
```

## Filtering
### Filtering, say, avgPrice <=30
Note: here $lte means less than or equal to see more [here](https://docs.strapi.io/developer-docs/latest/developer-resources/database-apis-reference/rest/filtering-locale-publication.html#filtering)
```
    baseUrl/api/appName?filters[avgPrice][$lte]=30
```

## Authentication

### registering a user
To register you have to send a post reqeust to the following url
```
    baseUrl/api/auth/local/register
```

### depending on your required fields you'll then send a json. Something like this:
```
{
    "username": "Example",
    "email": "example@example.com",
    "password": "password"
}
```

### after sending it, you'll get a jwt

## Acknowledgements
- Tutorial source: [Laith Academy](https://www.youtube.com/watch?v=vcopLqUq594&t=10s)
