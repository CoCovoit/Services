from quay.io/keycloak/keycloak:latest
# Use the official Keycloak image as a base
# Set the environment variable to enable the Keycloak server
ENV KC_BOOTSTRAP_ADMIN_USERNAME=admin1
ENV KC_BOOTSTRAP_ADMIN_PASSWORD=admin1
ENV KC_HOSTNAME_PORT=8081

# Expose the default Keycloak port
EXPOSE 8081

# Create 2 REALMS
COPY realms/*.json /opt/keycloak/data/import/

# Start Keycloak
CMD [ "start-dev", "--import-realm", "--http-port=8081" ]
