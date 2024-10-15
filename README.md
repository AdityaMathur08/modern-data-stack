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



