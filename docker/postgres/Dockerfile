FROM postgres:16-alpine

EXPOSE 5432

HEALTHCHECK --interval=10s --timeout=5s --start-period=10s --retries=5 \
  CMD pg_isready -U "$POSTGRES_USER" -d "$POSTGRES_DB"

STOPSIGNAL SIGTERM

CMD ["postgres"]
