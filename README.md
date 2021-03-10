# Purpose

Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Gulp/Grunt pre-installed.

Available on Docker Hub [[Gulp](https://hub.docker.com/r/mathieu79/dotnet-sdk-nodejs-gulp)/[Grunt](https://hub.docker.com/r/mathieu79/dotnet-sdk-nodejs-grunt)] - use `docker pull mathieu79/dotnet-sdk-nodejs-gulp` or `docker pull mathieu79/dotnet-sdk-nodejs-grunt` to get it.


# Ingredients

* Based on docker images from [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk)
* [NodeJS](https://nodejs.org/)
* [Gulp](https://gulpjs.com/)
* [Grunt](https://gruntjs.com/)
* [Webpack](https://webpack.js.org/)
