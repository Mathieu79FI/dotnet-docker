FROM mcr.microsoft.com/dotnet/sdk:7.0.407-alpine3.18 AS base

FROM base AS build
ENV NODE_VERSION 20.11.1
ENV NODE_DOWNLOAD_SHA f2d89932803bcac02f5759e1e2ac700bcc6eb8b575590b21abe1d14c59a9aedc
RUN curl -SL "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64-musl.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 --no-same-owner \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.90.3 webpack-cli@5.1.4

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
