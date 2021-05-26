FROM mcr.microsoft.com/dotnet/sdk:5.0.300-alpine3.13 AS base

FROM base AS build
ENV NODE_VERSION 14.17.0
ENV NODE_DOWNLOAD_SHA 7a2c5a69ca44ac1bf7e7fa7ec578e9da82f9187aa5cd8d551a877aeb57985e27
RUN curl -SL "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64-musl.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 --no-same-owner \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.37.1 webpack-cli@4.7.0

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
