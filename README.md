# Strapi Starter Gatsby Blog

Gatsby starter for creating a blog with Strapi.

This starter allows you to try Strapi with Gatsby with the example of a simple blog. It is fully customizable and due to the fact that it is open source, fully open to contributions. Do not hesitate to add new features etc ...

You may want to know how to develop such a starter by your own! This starter is actually the result of this [tutorial](https://strapi.io/blog/build-a-static-blog-with-gatsby-and-strapi)

![screenshot image](/screenshot.png)

### Deploy the backend

To deploy the Strapi instance you'll need:

- [An Heroku account](https://signup.heroku.com/) for free
- [A Cloudinary account for saving images](https://cloudinary.com/users/register/free) for free

Once you have created these accounts you can deploy your instance by clicking on this button

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/strapi/strapi-starter-blog)

[Here](https://github.com/strapi/strapi-starter-blog) is the repository of the backend of this starter

### Deploy the frontend

**On Netflify**

- [A Netilfy account](https://app.netlify.com/signup) for free

Once you have created your account, add the url of your Heroku instance  (without the trailing slash) as a parameter to the following url.

https://app.netlify.com/start/deploy?repository=https://github.com/strapi/strapi-starter-gatsby-blog#API_URL=<your-strapi-app.herokuapp.com>

- Visit this url to deploy your application

**On Vercel**

Coming soon...

**On Gatsby Cloud**

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

- Open your Strapi admin panel and go to `/admin/settings/webhooks`
- Create a new Webhook with following properties:
  - Name: `Gatsby Cloud`
  - Url: The first Webhook Url Gatsby Cloud provide in your Gatsby Dashboard Sites. It should be something like this: `https://webhook.gatsbyjs.com/hooks/data_source/` without the `/publish/`
  - Check every Events for `Entry` and `Media`

That's it! Now Strapi will inform Gatsby Cloud to build your Gatsby project everytime you create/update/delete content

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

**Backend**

See full instructions [here](https://github.com/strapi/strapi-starter-blog)

**Frontend**

```bash
git clone https://github.com/strapi/strapi-starter-gatsby-blog.git
cd strapi-starter-gatsby-blog
```

#### Start the frontend server

```bash
# Using yarn
yarn install
yarn develop

# Using npm
npm install
npm run develop
```

Gatsby server is running here => [http://localhost:8000](http://localhost:8000)

Enjoy this starter
