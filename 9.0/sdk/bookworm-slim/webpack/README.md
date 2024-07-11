# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Webpack pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):9.0.100-preview.6-bookworm-slim
* [NodeJS](https://nodejs.org/) 20.15.1
* [Webpack](https://www.npmjs.com/package/webpack) 5.92.1
* [Webpack-cli](https://www.npmjs.com/package/webpack-cli) 5.1.4
* [TypeScript](https://www.npmjs.com/package/typescript) 5.5.3
* [PostCSS](https://www.npmjs.com/package/postcss) 8.4.39
* [postcss-loader](https://www.npmjs.com/package/postcss-loader) 8.1.1

# Full Tag Listing
## Linux amd64 tags
- [`6.0.424-bullseye-slim`, `6.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/bullseye-slim/webpack/Dockerfile)
- [`6.0.424-alpine`, `6.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/alpine/webpack/Dockerfile)
- [`8.0.303-bookworm-slim`, `8.0-sdk`, `latest` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/8.0/sdk/bookworm-slim/webpack/Dockerfile)
- [`8.0.303-alpine`, `8.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/8.0/sdk/alpine/webpack/Dockerfile)
- [`9.0.100-preview.6-bookworm-slim`, `9.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/9.0/sdk/bookworm-slim/webpack/Dockerfile)
