To install keycloak dev mode (non-production):
docker run -d -p 8080:8080 -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=your-password -e KC_HOSTNAME_STRICT=false -e KC_HOSTNAME_STRICT_HTTPS=false -e KC_HTTP_ENABLED=true quay.io/keycloak/keycloak:latest start-dev

/opt/keycloak/bin/kcadm.sh config credentials --server http://185.129.118.64:8080 --realm master --user admin --password your-password
/opt/keycloak/bin/kcadm.sh update realms/master -s sslRequired=NONE
