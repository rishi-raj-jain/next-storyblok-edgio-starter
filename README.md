# Next.js Storyblok Edgio Boilerplate

This repository is a [Next.js](https://nextjs.org) [Storyblok](https://www.storyblok.com) [Edgio](https://edg.io) starter template used in following [guide](https://www.storyblok.com/tp/<upcoming-url>).

## Requirements

To use this project you have to have a Storyblok and Edgio account. If you don't have one yet you can register at [Storyblok](https://www.storyblok.com) and [Edgio](https://app.layer0.co), both are free!

## How to get started?

Read the [Next.js tutorial](https://www.storyblok.com/tp/add-a-headless-cms-to-next-js-in-5-minutes) about connecting Storyblok and Next.js

### 1. Clone the repo

```bash
git clone https://github.com/rishi-raj-jain/next-storyblok-edgio-starter.git
```

### 2. Install Dependencies

```bash
npm install
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

```bash
npm run dev
```

### 5. Install Edgio CLI

```bash
npm i -g @edgio/cli
edgio init
```

### 5. Run a production build of your app and test it locally

```bash
edgio build && edgio run --production
```

### 6. Deploy to Edgio

```bash
edgio deploy
```

### 7. (Optional) Add Environment Variables on Edgio Console

Follow [this section](https://www.storyblok.com/tp/<upcoming-url>#<upcoming-section>) of guide to add STORYBLOK_API_TOKEN and EDGIO_DEPLOY_TOKEN for integrating it with GitHub Workflows.

## Resources

- [Next.js docs](https://nextjs.org/docs/#setup)
- [Storyblok Tutorial](https://www.storyblok.com/tp/add-a-headless-cms-to-next-js-in-5-minutes)
- [Preview Mode](https://nextjs.org/docs/advanced-features/preview-mode)
- [Edgio Deploy Guide](https://docs.edg.io/guides/deploying)
