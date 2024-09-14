# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Webpack pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):6.0.425-1-alpine3.19
* [NodeJS](https://nodejs.org/) 20.17.0
* [Webpack](https://www.npmjs.com/package/webpack) 5.94.0
* [Webpack-cli](https://www.npmjs.com/package/webpack-cli) 5.1.4
* [TypeScript](https://www.npmjs.com/package/typescript) 5.6.2
* [PostCSS](https://www.npmjs.com/package/postcss) 8.4.45
* [postcss-loader](https://www.npmjs.com/package/postcss-loader) 8.1.1

# Full Tag Listing
## Linux amd64 tags
- [`6.0.425-bullseye-slim`, `6.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/bullseye-slim/webpack/Dockerfile)
- [`6.0.425-alpine`, `6.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/alpine/webpack/Dockerfile)
