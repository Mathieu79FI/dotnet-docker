FROM mcr.microsoft.com/dotnet/sdk:8.0.401-1-alpine3.19 AS base

FROM base AS build
ENV NODE_VERSION=20.17.0
ENV NODE_DOWNLOAD_SHA=16aee679dc57b5399af2ae3942fb5a9a723a7cbf9c4497c1656fcc5d1423b797
RUN curl -SL "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64-musl.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 --no-same-owner \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.94.0 webpack-cli@5.1.4 typescript@5.6.2 postcss@8.4.45 postcss-loader@8.1.1

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
