# Installation

Call the Vite / Svelte installation and select `svelte` and then `svelte-ts`.

```
npm init vite@latest

cd std-cards-dev

npm install

npm run dev
```

Install Tailwind and DaisyUI

```
npm install -D tailwindcss@latest postcss@latest autoprefixer@latest

npm install daisyui

npx tailwindcss init -p
```

Before we edit any file we initialize git.

```
git init && git add -A && git commit -m "Initial commit"
```

Edit the Tailwind configuration file: `tailwind.config.cjs

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['./index.html', './src/**/*.svelte'],
  theme: {
    extend: {},
  },
  plugins: [require('daisyui')],
};
```

Edit the Postcss configuration file (which should be OK): `postcss.config.js`

```
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```

Edit the global CSS file: `app.css`

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
