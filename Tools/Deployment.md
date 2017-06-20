Deployment
===========

[Roast.io](https://www.roast.io/)
-------------------------------------

A command line service for deploying static web apps, quickly and with no fuss.

CLI repo: [roast-io-node-cli](https://github.com/sanfrancesco/roast-io-node-cli)

### Key features

- Super simple to use, **no config**
- Built in **Server Side Rendering** - Serves the rendered DOM of each route in the app from the server,
  then React takes over. This makes the initial load very fast
- Built in support for the **HTML5 History API**, page reload on any route just works
- Reasonable limits on the free account

### Easy setup

- Sign up on roast.io
- `npm i -g roast` (anywhere)
- `roast deploy -p dist` (in project root, `dist` is the build folder)

#### To add as a `deploy` script in `package.json`:

- Add `"deploy": "roast deploy -p dist"` under `scripts`
- Run `npm run deploy`

### Why not GitHub Pages

- `node_modules` and `dist` folders are usually ignored (in `.gitignore`) and not pushed.
- Even if we removed them from `.gitignore` and pushed, the link for GitHub Pages would have to contain `/dist` at the end.  
- HTML5 History API (URL’s without the `#` sign) require a server that redirects unknown URLs to `index.html`, this is not supported.

### Comparing to [Surge.sh](https://surge.sh/)

- HTML5 History API support on Surge requires some weird hacks since it doesn't support it by default
- Requires `.surgeignore` file - Surge ignores `node_modules` folders by default (see <https://github.com/surge-sh/ignore>),
  but webpack creates a `node_modules` folder under the `_` folder in our `dist` folder (which we want to deploy), Roast doesn’t ignore it

[Now](https://zeit.co/now)
---------------------------

A command line service for deploying Node.js servers, with minimal configuration.
