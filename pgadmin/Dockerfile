FROM dpage/pgadmin4:4.20

COPY servers.json /pgadmin4/servers.json
COPY --chown=pgadmin:pgadmin pgpass-localdb /var/lib/pgadmin/storage/user_domain.com/pgpass-localdb

COPY --chown=pgadmin:pgadmin lab-entrypoint.sh /lab-entrypoint.sh
RUN chmod +x /lab-entrypoint.sh

ENTRYPOINT ["/lab-entrypoint.sh"]
