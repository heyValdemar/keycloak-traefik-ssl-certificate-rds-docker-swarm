# Keycloak with Amazon RDS and SSL Certificate in a Docker Swarm

Create Amazon RDS database instance, configure Traefik and create secrets for storing the passwords on the Docker Swarm manager node before applying the configuration.

Traefik configuration: https://github.com/heyValdemar/traefik-ssl-certificate-docker-swarm

Create a secret for storing the password for Keycloak database using the command:

`printf "YourPassword" | docker secret create keycloak-postgres-password -`

Create a secret for storing the password for Keycloak administrator using the command:

`printf "YourPassword" | docker secret create keycloak-application-password -`

Clear passwords from bash history using the command:

`history -c && history -w`

Deploy Keycloak in a Docker Swarm using the command:

`docker stack deploy -c keycloak-traefik-ssl-certificate-rds-docker-swarm.yml keycloak`
