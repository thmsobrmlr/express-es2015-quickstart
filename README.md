## Usage

Expand quickstart template

    mkdir my-new-project && cd my-new-project

    git clone https://github.com/thomas88/express-es2015-quickstart.git . &&
      rm -rf .git/  && rm LICENSE && rm README.md

Initialize node package

    npm init

Install dependencies

    npm install --save-dev babel-cli babel-eslint babel-preset-es2015 babel-watch \
      eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y \
      eslint-plugin-react chalk localtunnel

    npm install --save express body-parser dotenv

Add build scripts to `package.json`

    "main": "build/index.js",
    "scripts": {
      "lint": "eslint source",
      "dev": "babel-watch source/index.js",
      "clean": "rm -rf build/* && mkdir build",
      "build": "babel source -d build",
      "start": "node build/index.js",
      "debug": "node --debug build/index.js",
      "tunnel": "babel-node scripts/tunnel.js"
    },
