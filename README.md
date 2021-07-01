# Next.js Storyblok Layer0 Boilerplate

This repository is a [Next.js](https://nextjs.org) [Storyblok](https://www.storyblok.com) [Layer0](https://layer0.co) starter template used in following [guide](https://www.storyblok.com/tp/<upcoming-url>).

## Requirements

To use this project you have to have a Storyblok and Layer0 account. If you don't have one yet you can register at [Storyblok](https://www.storyblok.com) and [Layer0](https://layer0.co), both are free!

## How to get started?

Read the [Next.js tutorial](https://www.storyblok.com/tp/add-a-headless-cms-to-next-js-in-5-minutes) about connecting Storyblok and Next.js

### 1. Clone the repo

```sh
  $ git clone https://github.com/rishi-raj-jain/next-storyblok-layer0-starter.git
```

### 2. Install all dependencies

```sh
$  npm install && npm install --only=dev
```

### 3. Adding the Access token

Create a new empty Space and exchange the preview token with your own in `lib/storyblok.js`.

```js
// in lib/storyblok.js
const Storyblok = new StoryblokClient({
  accessToken: "your-preview-token", // process.env.STORYBLOK_API_TOKEN (refer to .env.example)
  cache: {
    clear: "auto",
    type: "memory",
  },
});
```

### 4. Run your project

Set the preview domain in <strong>Storyblok</strong> to `http://localhost:3000/`

```sh
# to run in developer mode
$ npm run dev # or yarn dev
```

### 5. Install Layer0 CLI

```sh
$ npm i -g @layer0/cli # or yarn global add @layer0/cli
$ layer0 init
```

### 5. Run a production build of your app and test it locally

```sh
$ layer0 build && layer0 run --production
```

### 6. Deploy to Layer0

```sh
$ layer0 deploy
```

### 7. (Optional) Add Environment Variables on Layer0 Console

Follow [this section](https://www.storyblok.com/tp/<upcoming-url>#<upcoming-section>) of guide to add StoryBlok Token and Layer0_Deploy_Token for integrating it with GitHub Workflows.

## Resources

- [Next.js docs](https://nextjs.org/docs/#setup)
- [Storyblok Tutorial](https://www.storyblok.com/tp/add-a-headless-cms-to-next-js-in-5-minutes)
- [Preview Mode](https://nextjs.org/docs/advanced-features/preview-mode)
- [Layer0 Deploy Guide](https://docs.layer0.co/guides/deploying)
