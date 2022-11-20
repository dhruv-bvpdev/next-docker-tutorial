# With Docker

This examples shows how to use Docker with Next.js based on the [deployment documentation](https://nextjs.org/docs/deployment#docker-image).

## How to use

```bash
git clone https://github.com/dhruv-bvpdev/next-docker-tutorial.git

cd next-docker-tutorial
```

## Using Docker

> Make sure you have docker installed and configured on your machine

1. Build your container: `docker build -t <ramdom_name_of_container> .`
2. Run your container: `docker run -p 3000:3000 <random_name_of_container>`

You can view your images created with `docker image ls`.

> Once the project is built you can deploy it using any of hosting services like fly.io, aws, heroku, digital ocean etc

### In existing projects

To add support for Docker to an existing project, just copy the `Dockerfile` into the root of the project and add the following to the `next.config.js` file:

```js
// next.config.js
module.exports = {
  // ... rest of the configuration.
  output: 'standalone'
}
```

This will build the project as a standalone app inside the Docker image.

## Running Locally

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.ts`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.ts`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.
