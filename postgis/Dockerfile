FROM usgsastro/postgres:latest

RUN apt-get update && apt-get install -y    \
        postgis                             \
        postgresql-13-postgis-3             \
        postgresql-13-postgis-3-scripts     \
    && rm -rf /var/cache/apt/* &&           \
    rm -rf /var/lib/apt/lists/*


