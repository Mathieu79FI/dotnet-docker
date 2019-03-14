# Purpose

Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Gulp pre-installed.

Available on [Docker Hub](https://hub.docker.com/r/mathieu79/dotnet-sdk-nodejs-gulp) - use `docker pull mathieu79/dotnet-sdk-nodejs-gulp` to get it.


# Ingredients

* Based on docker images from [mcr.microsoft.com/dotnet/core/sdk](https://hub.docker.com/_/microsoft-dotnet-core-sdk/)
* [NodeJS](https://nodejs.org/)
* [Gulp](https://gulpjs.com/)
