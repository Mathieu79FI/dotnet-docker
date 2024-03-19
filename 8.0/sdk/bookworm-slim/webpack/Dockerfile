FROM mcr.microsoft.com/dotnet/sdk:8.0.203-bookworm-slim AS base

FROM base AS build
ENV NODE_VERSION 20.11.1
ENV NODE_DOWNLOAD_SHA bf3a779bef19452da90fb88358ec2c57e0d2f882839b20dc6afc297b6aafc0d7
RUN curl -SL "https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}-linux-x64.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.90.3 webpack-cli@5.1.4

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
