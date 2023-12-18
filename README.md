### Docker Compose Solution

The application is deployed using [Docker Compose](https://docs.docker.com/compose/), which can be found in the [docker-compose.yml](../../../docker-compose.yml) file.

Below is a visual representation of the solution:

| ![Docker Compose Solution](../../../docs/diagrams/docker-compose-solution.png) |
|:------------------------------------------------------------------------------:|
|                       *Docker Compose solution diagram*                        |

#### Services

#### db-tests

> [!NOTE] 
> This service provides a PostgreSQL database specifically tailored for testing purposes.
> 
> The database is pre-configured with user credentials and a default database schema.
> 
> Exposes a port for external access. 

[Dockerfile](../tests/Dockerfile-db-test)

#### spring

> [!NOTE]
> This service encapsulates a scalable JVM Spring application that provides the Gomoku Royale REST API.
>
> Utilizes the PostgreSQL database provided by the `db-tests` service for data storage.
>
> Configured to run on a specific port for external access.

[Dockerfile](../tests/Dockerfile-spring)

#### nginx

> [!NOTE]
> Nginx service serving a load balancer for the scalable `spring-service` JVM application.
>
> Listens for requests on an external port, which the clients connect to, and forwards the requests using a defined strategy.
> 
> Configuration can be found in the [nginx.conf](../tests/nginx/nginx.conf) file.

[Dockerfile](../tests/Dockerfile-nginx)

#### ubuntu

> [!NOTE]
> Ubuntu machine serving as a diagnostic and debugging tool within the Docker Compose environment.
>
> Provides an interactive shell for direct interaction.
>
> Includes 'dig' for DNS-related observations or testing.
>
> Useful for monitoring and understanding the Docker Compose network and container interactions.

[Dockerfile](../tests/Dockerfile-ubuntu)