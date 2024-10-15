# modern-data-stack
Implementing data architecture for data pipelines using components used in modern data stack


## Setup-guide:
### Tech Stack:


### Database

CONNECT TO PG
=========
Run Command via Terminal:
- Link: https://docs.docker.com/engine/reference/commandline/container_exec/
- Examples:
   - docker exec -ti NAME_OF_CONTAINER psql -U POSTGRES_USER
   - docker exec -ti environment-postgres-1 psql -U postgres 

INTERFACE
=========
CloudBeaver Community - Interface
- Link: https://github.com/dbeaver/cloudbeaver

S.no|Service| Username | Credentials | Hostname |
|---|------|----------|-------------|----------|
1.|Database(Postgres)|postgres||172.99.0.2(container)
2.|Cloud Beaver Database workbench| cbadmin  |  | 172.99.0.2 |
3.|Airbyte on Local|airbyte|password||


AIRBYTE
==========
We have airbyte running in containers to start it up, following link is helpful:
https://www.restack.io/docs/airbyte-knowledge-airbyte-docker-container-guide

Please note since this is a differnt git repo, we have it in a differnt folder structure in environment.
TODO: Add the service in the project's main dockerfile

git clone https://github.com/airbytehq/airbyte.git
cd airbyte
./run-ab-platform.sh

Access Airbyte: Open your web browser and go to http://localhost:8000 to access the Airbyte interface.

Default Credentials: Log in using the default username airbyte and password password. Remember to update these credentials in your .env file for security.

Begin Data Syncing: Once logged in, you can start configuring your data sources and destinations to begin syncing data.

### Roles and Permissions:

-- ESTABLISH ROLE HEIRARCHY

### Roles and Permissions:

-- ESTABLISH ROLE HEIRARCHY

```plaintext
Analyst
    > Developer (inherits Analyst Role)
        > Automation (inherits Developer Role & Analyst Role)
Loader
```



