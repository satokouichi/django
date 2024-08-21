ARG POSTGRES_VERSION
FROM postgres:${POSTGRES_VERSION}

COPY ./postgresql.conf /etc/postgresql/postgresql.conf
RUN chmod 644 /etc/postgresql/postgresql.conf