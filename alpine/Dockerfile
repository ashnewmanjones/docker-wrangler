FROM alpine:3.10

RUN wget --quiet -O /tmp/wrangler.tar.gz "https://github.com/cloudflare/wrangler/releases/download/v1.6.0-rc.0/wrangler-v1.6.0-rc.0-x86_64-unknown-linux-musl.tar.gz"; \
    tar xzvf /tmp/wrangler.tar.gz -C /usr/local/bin wrangler-v1.6.0-rc.0-x86_64-unknown-linux-musl/wrangler --strip-components 1; \
    rm -f /tmp/wrangler.tar.gz; \
    chmod +x /usr/local/bin/wrangler

COPY entrypoint.sh /
ENTRYPOINT [ "/entrypoint.sh" ]
CMD ["wrangler"]
