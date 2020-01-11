# Amy's Portfolio

This is a static web app created using [Svelte](https://svelte.dev/).

The idea of this site is to allow people to see the work of Amy Dickson, an Architectural Technology student at Edinburgh Napier University.

See the latest production of this website at [https://amy-dickson.com](https://amy-dickson.com).


## Development

From the project route, install the dependencies...

```
npm install
```

Run locally using [Rollup](https://rollupjs.org):

```bash
npm run dev
```

This will run your app at [localhost:5000](http://localhost:5000).

## Building and running in production mode

To create aproduction build of the app:
```bash
npm run build
```

You can run the production build app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv).


## Deploying to the web

The app is currently deployed on an AWS bucket.

To deploy, build using `npm run build` and then copy/paste the contents of the `./public/` folder to an S3 bucket.
