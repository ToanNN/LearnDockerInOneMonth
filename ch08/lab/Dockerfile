FROM diamol/node

ENV MAX_ALLOCATION_MB=4096 \
    LOOP_ALLOCATION_MB=512 \
    LOOP_INTERVAL_MS=2000

CMD ["node", "memory-hog.js"]

HEALTHCHECK --interval=5s --timeout=30s --start-period=5s --retries=3 CMD [ "node" , "memory-check.js" ]
WORKDIR /app
COPY src/ .