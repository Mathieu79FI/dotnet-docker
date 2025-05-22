# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Webpack pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):10.0.100-preview.4-trixie-slim
* [NodeJS](https://nodejs.org/) 22.16.0
* [Webpack](https://www.npmjs.com/package/webpack) 5.99.9
* [Webpack-cli](https://www.npmjs.com/package/webpack-cli) 6.0.1
* [TypeScript](https://www.npmjs.com/package/typescript) 5.8.3
* [PostCSS](https://www.npmjs.com/package/postcss) 8.5.3
* [postcss-loader](https://www.npmjs.com/package/postcss-loader) 8.1.1

# Full Tag Listing
## Linux amd64 tags
- [`8.0.409-bookworm-slim`, `8.0-sdk`, `latest` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/8.0/sdk/bookworm-slim/webpack/Dockerfile)
- [`8.0.409-alpine`, `8.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/8.0/sdk/alpine/webpack/Dockerfile)
- [`9.0.300-bookworm-slim`, `9.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/9.0/sdk/bookworm-slim/webpack/Dockerfile)
- [`9.0.300-alpine`, `9.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/9.0/sdk/alpine/webpack/Dockerfile)
- [`10.0.100-preview.4-trixie-slim`, `10.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/10.0/sdk/trixie-slim/webpack/Dockerfile)
