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

### Scaffold your project

This command will launch both of your backend and frontend server and do a data migration in your backend server

```bash
# Using yarn
yarn build:yarn
yarn develop:yarn

# Using npm
npm run build:npm
npm run develop:npm
```

Alternatively, you can still start your servers separately:

### Start the backend server

```bash
cd backend

# Using yarn
yarn build
yarn develop

# Using npm
npm run build
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

## Gatsby Cloud

You may want to deploy this starter frontend on [Gatsby Cloud](https://www.gatsbyjs.com/dashboard) in order to try the Gatsby Preview maybe!

- Fork this starter on your own Github account
- Create a new site by choosing the option "I already have a Gatsby site"

![Create a New site](/medias/create-a-new-site.png)

You'll be asked to select the repository you want to use

- Select your new Strapi Starter Gatsby Blog repository you just forked and specify the Gatsby project folder which is `frontend` in this starter

![Repository](/medias/repository.png)

- You can then copy the webhook url and skip this step

![Skip step](/medias/skip.png)

- Paste your Strapi `API_URL` for both of your `Builds Environment variables` and `Preview Environment variables` (we consider that you deployed your strapi server)

![Env](/medias/env.png)

Now you'll need to create a Webhook on your strapi server in order to tell Gatsby cloud to build your Gatsby project each time your create/update/delete content

- Open your Strapi admin panel and go to [Webhooks](http://localhost:1337/admin/settings/webhooks)
- Create a new Webhook with following properties:
  - Name: `Gatsby Cloud`
  - Url: The first Webhook Url Gatsby Cloud provide in your Gatsby Dashboard Sites. It should be something like this: `https://webhook.gatsbyjs.com/hooks/data_source/` without the `/publish/`
  - Check every Events for `Entry` and `Media`

That's it! Now Strapi will inform Gatsby Cloud to build your Gatsby project everytime you create/update/delete content

![Env](/medias/gif.gif)

Enjoy this starter
