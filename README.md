# Introduction

When setting yarn PnP `cacheFolder` to a different drive than `C` Storybook crashes. There is a broken path containing both `C` and `D` drives: `C:\Users\rawf\projects\storybook-pnp-issues\D:\yarn\@storybook-manager-npm-7.0.26-ce3e1a67d5-4912726b5d.`

```
yarn storybook
@storybook/cli v7.0.26

ERR! Error: Failed to load static files, no such directory: C:\Users\rawf\projects\storybook-pnp-issues\D:\yarn\@storybook-manager-npm-7.0.26-ce3e1a67d5-4912726b5d.zip\node_modules\@storybook\manager\static
ERR! Make sure this directory exists, or omit the -s (--static-dir) option.
ERR!     at parseStaticDir (d:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\presets\common-preset.js:1:2914)
ERR!     at <anonymous> (d:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\presets\common-preset.js:4:842)
ERR!     at async Promise.all (index 0)
ERR!     at Object.favicon2 (d:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\presets\common-preset.js:4:604)
ERR!     at async useStatics (D:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\index.js:11:6846)
ERR!     at async Promise.all (index 2)
ERR!     at async storybookDevServer (D:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\index.js:46:6177)
ERR!     at async buildDevStandalone (D:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\index.js:59:2786)
ERR!     at async withTelemetry (D:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\index.js:46:3620)
ERR!     at async dev (D:\yarn\@storybook-cli-npm-7.0.26-681f8ca0fa-94dc69a519.zip\node_modules\@storybook\cli\dist\generate.js:440:401)
ERR!  Error: Failed to load static files, no such directory: C:\Users\rawf\projects\storybook-pnp-issues\D:\yarn\@storybook-manager-npm-7.0.26-ce3e1a67d5-4912726b5d.zip\node_modules\@storybook\manager\static
ERR! Make sure this directory exists, or omit the -s (--static-dir) option.
ERR!     at parseStaticDir (d:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\presets\common-preset.js:1:2914)
ERR!     at <anonymous> (d:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\presets\common-preset.js:4:842)
ERR!     at async Promise.all (index 0)
ERR!     at Object.favicon2 (d:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\presets\common-preset.js:4:604)
ERR!     at async useStatics (D:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\index.js:11:6846)
ERR!     at async Promise.all (index 2)
ERR!     at async storybookDevServer (D:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\index.js:46:6177)
ERR!     at async buildDevStandalone (D:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\index.js:59:2786)
ERR!     at async withTelemetry (D:\yarn\@storybook-core-server-npm-7.0.26-0589c8b6a6-5fea5e8ae2.zip\node_modules\@storybook\core-server\dist\index.js:46:3620)
ERR!     at async dev (D:\yarn\@storybook-cli-npm-7.0.26-681f8ca0fa-94dc69a519.zip\node_modules\@storybook\cli\dist\generate.js:440:401)
```

## Sample project setup

Sample project is based on `create-react-app` with the TypeScript template enabled. Storybook installed using [documentation](https://storybook.js.org/docs/7.0/react/get-started/install) `npx storybook@latest init`.
The `cacheFolder` set to `D:\\yarn` in the `.yarnrc.yml` file.

## Versions

```
Windows 11 Pro 64-bit
NodeJs v18.16.0
npm 9.5.1
yarn 3.6.1
```
