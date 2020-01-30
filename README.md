# Strapi Starter Gatsby Blog

Gatsby starter for creating a static blog with Strapi.

This starter allows you to try Strapi with Gatsby with the example of a simple static blog. It is fully customizable and due to the fact that it is open source, fully open to contributions. Do not hesitate to add new features etc ...

You may want to know how to develop such a starter by your own! This starter is actually the result of this [tutorial](https://strapi.io/blog/build-a-static-blog-with-gatsby-and-strapi)

![screenshot image](/screenshot.png)

### Features

- 2 Content types: Article, Category
- Permissions set to `true` for article and category
- Responsive design using UIkit

### Pages

- "/" display every articles
- "/articles/:id" display one article
- "/category/:id" display articles depending on the category

### Getting started

**Clone the repository and install dependencies**

```
git clone https://github.com/strapi/strapi-starter-gatsby-blog.git
cd strapi-starter-gatsby-blog
yarn setup
```

### Run your Strapi backend

```
cd backend
strapi dev
```

Server is running here => [http://localhost:1337](http://localhost:1337)

### Run your Gatsby frontend

```
cd frontend
gatsby develop
```

Server is running here => [http://localhost:8000](http://localhost:8000)

### What you need to do

Create your admin user and after that you'll only need to create your articles and your categories
To do this, head to your strapi admin panel just right here => [http://localhost:1337/admin](http://localhost:1337/admin)

Enjoy this starter
