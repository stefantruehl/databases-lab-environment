FROM dpage/pgadmin4:4.18

COPY servers.json /pgadmin4/servers.json
COPY --chown=pgadmin:pgadmin pgpass-localdb /var/lib/pgadmin/storage/user_domain.com/pgpass-localdb
