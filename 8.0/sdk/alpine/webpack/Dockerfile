FROM mcr.microsoft.com/dotnet/sdk:8.0.409-alpine3.21 AS base

FROM base AS build
ENV NODE_VERSION=22.16.0
ENV NODE_DOWNLOAD_SHA=6d20ac7f034c4117bbefcbde6b63412637dba30aab144a1114fc604b6609fcba
RUN curl -SL "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64-musl.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 --no-same-owner \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.99.9 webpack-cli@6.0.1 typescript@5.8.3 postcss@8.5.3 postcss-loader@8.1.1

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
