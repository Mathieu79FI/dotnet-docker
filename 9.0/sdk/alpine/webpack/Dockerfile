FROM mcr.microsoft.com/dotnet/sdk:9.0.200-alpine3.20 AS base

FROM base AS build
ENV NODE_VERSION=22.14.0
ENV NODE_DOWNLOAD_SHA=6b50f327fd5053b5e4ba67de4bf93aa23653d8a9de39bd6f905f839069c7933d
RUN curl -SL "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64-musl.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 --no-same-owner \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.98.0 webpack-cli@6.0.1 typescript@5.7.3 postcss@8.5.2 postcss-loader@8.1.1

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
