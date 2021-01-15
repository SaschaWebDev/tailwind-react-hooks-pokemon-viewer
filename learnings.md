# Learnings

## Installation

This project was created with npm instead of yarn and can be reproduces with the following commands

```
npx create-react-app pokemon-hooks --use-npm

cd pokemon-hooks

npm install tailwindcss@npm:@tailwindcss/postcss7-compat @tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9 react-router-dom

npm install @craco/craco
```

Then overwrite the package.json scripts

```
  "start": "craco start",
  "build": "craco build",
  "test": "craco test"
```

Create a craco.config.js file:

```
module.exports = {
  style: {
    postcss: {
      plugins: [
        require('tailwindcss'),
        require('autoprefixer'),
      ],
    },
  },
}
```

Then use the tailwind initial

```
npx tailwindcss init
```

Overwrite the purge command within the tailwind.config.js

```
purge: ['./src/**/*.{js,jsx,ts,tsx}', './public/index.html'],
```

Paste this within your index.css

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
