FROM mcr.microsoft.com/dotnet/sdk:10.0.100-preview.4-trixie-slim AS base

FROM base AS build
ENV NODE_VERSION=22.16.0
ENV NODE_DOWNLOAD_SHA=fb870226119d47378fa9c92c4535389c72dae14fcc7b47e6fdcc82c43de5a547
RUN curl -SL "https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}-linux-x64.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.99.9 webpack-cli@6.0.1 typescript@5.8.3 postcss@8.5.3 postcss-loader@8.1.1

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
