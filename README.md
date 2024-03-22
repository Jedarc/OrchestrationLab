# OrchestrationLab

A simple proof of concept (POC) of the Orchestrator Pattern.


## Prerequisites

* [Docker](https://www.docker.com/products/docker-desktop/) 🐋
* [Visual Studio 2022](https://visualstudio.microsoft.com/pt-br/downloads/) or above. 🔨
* [.Net 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) 📦


## Configuration

### 1. Set the values of the environment variables.
At the file `/src/docker-compose/.env`, fill the value for each variable.

### 2. Set the Startup Project
Ensure that the `docker-compose.dcproj` is the default **project** to start running in Visual Studio.

### 3. (Optional) Change applications ports
If you have a conflict with any port in use, 
simply change it in the `src\docker-compose\docker-compose.yml` file 
(remember that the value to be changed is the one to the left side of the colon punctuation), 
and then update the mapping of the respective service in the reverse proxy (Traefik), 
in the file `src\docker-compose\services\traefik\dynamic.yml`. 
Ready! Everything else in the application will be using the proxy URL, so don't worry.

## TODO

- [x] Add integrated docker-compose to Visual Studio.
- [x] **(Partial with .env)** Add user secrets support.
- [ ] Add RabbitMQ (DL, DM)
- [x] Add Traefik.
- [ ] Add Redis.
- [ ] Add PostgreSQL.
- [ ] Add Health Check to services and providers.
- [ ] Add Polly (consider number of hits to turn off worker).
- [ ] Add Relay Worker (to turn workers on again based on service health).
- [ ] Add Providers Mock.
- [ ] Add unit tests.
- [ ] Add stress tests (JMeter?).
- [ ] Add MongoDB for auditing.
- [ ] Add API versioning.
- [ ] Add webhook.
- [ ] Add Kibana logging.