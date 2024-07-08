FROM mcr.microsoft.com/dotnet/sdk:8.0.302-1-bookworm-slim AS base

FROM base AS build
ENV NODE_VERSION 20.15.0
ENV NODE_DOWNLOAD_SHA 3a873874caae30b5a9125fdf8872f7800cc0216eb89d097470110cd267a596e2
RUN curl -SL "https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}-linux-x64.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA  nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
    && npm install --global webpack@5.92.1 webpack-cli@5.1.4 typescript@5.5.3 postcss@8.4.39 postcss-loader@8.1.1

FROM base AS final
COPY --from=build /usr/local/bin /usr/local/bin
COPY --from=build /usr/local/include /usr/local/include
COPY --from=build /usr/local/lib /usr/local/lib
COPY --from=build /usr/local/share /usr/local/share
COPY --from=build /root/.npm /root/.npm
