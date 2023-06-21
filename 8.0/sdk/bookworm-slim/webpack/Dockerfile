FROM mcr.microsoft.com/dotnet/sdk:8.0.100-preview.5-bookworm-slim AS base

FROM base AS build
ENV NODE_VERSION 20.3.0
ENV NODE_DOWNLOAD_SHA 80238ee1a9dee6b0d5d1081503c6fdd1c7f81bdf4ca6abd90aa5a568712a2eaa
RUN curl -SL "https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}-linux-x64.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.87.0 webpack-cli@5.1.4

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
