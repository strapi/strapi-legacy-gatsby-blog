# Strapi Starter Gatsby Blog

Gatsby starter for creating a static blog with Strapi.

This starter allows you to try Strapi with Gatsby with the example of a simple static blog. It is fully customizable and due to the fact that it is open source, fully open to contributions. Do not hesitate to add new features etc ...

You may want to know how to develop such a starter by your own! This starter is actually the result of this [tutorial](https://strapi.io/blog/build-a-static-blog-with-gatsby-and-strapi)

![screenshot image](/screenshot.png)

### Features

- 2 Content types: Article, Category
- 2 Created articles
- 3 Created categories
- Permissions set to `true` for article and category
- Responsive design using UIkit

### Pages

- "/" display every articles
- "/article/:id" display one article
- "/category/:id" display articles depending on the category

### Getting started

**Clone the repository and install dependencies**

```bash
git clone https://github.com/strapi/strapi-starter-gatsby-blog.git
cd strapi-starter-gatsby-blog

# Using yarn
yarn setup:yarn

# Using npm
npm run setup:npm
```

### Start the backend and frontend servers

```bash
# Using yarn
yarn develop:yarn

# Using npm
npm run develop:npm
```

Alternatively, you can still start your servers separately:

### Start the backend server

```bash
cd backend

# Using yarn
yarn develop

# Using npm
npm run develop
```

### Start the frontend server

```bash
cd frontend

# Using yarn
yarn develop

# Using npm
npm run develop
```

Gatsby server is running here => [http://localhost:8000](http://localhost:8000)
Strapi server is running here => [http://localhost:1337](http://localhost:1337)

Enjoy this starter
