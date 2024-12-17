FROM mcr.microsoft.com/dotnet/sdk:9.0.101-alpine3.20 AS base

FROM base AS build
ENV NODE_VERSION=22.12.0
ENV NODE_DOWNLOAD_SHA=8d96de0293fc3978d09e2a3fee68c66bca4efcca90f52105e6f7463636e97308
RUN curl -SL "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64-musl.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 --no-same-owner \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.97.1 webpack-cli@5.1.4 typescript@5.7.2 postcss@8.4.49 postcss-loader@8.1.1

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
