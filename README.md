# hasura-multi-schema-stack
Quick starter to locally test schema diff multiple version comparison and replication of hasura postgres stacks.

Subfolder name for project scope with auto docker compose prefix naming

`hasura-multi-schema`


## Expected output
```shell
docker ps

CONTAINER ID        IMAGE                          COMMAND                  CREATED             STATUS              PORTS                    NAMES
4aa255b33c3b        hasura/graphql-engine:v1.3.0   "graphql-engine serve"   29 seconds ago      Up 25 seconds       0.0.0.0:8082->8080/tcp   hasura-multi-schema_gql_he2_1
2e46770ab154        hasura/graphql-engine:v1.3.0   "graphql-engine serve"   29 seconds ago      Up 25 seconds       0.0.0.0:8081->8080/tcp   hasura-multi-schema_gql_he1_1
10a6756ba889        hasura/graphql-engine:v1.3.0   "graphql-engine serve"   29 seconds ago      Up 25 seconds       0.0.0.0:8083->8080/tcp   hasura-multi-schema_gql_he3_1
e994ce20de85        postgres:12                    "docker-entrypoint.s…"   29 seconds ago      Up 28 seconds       0.0.0.0:5453->5432/tcp   hasura-multi-schema_pg_3_1
f57a477b0a3d        postgres:12                    "docker-entrypoint.s…"   29 seconds ago      Up 28 seconds       0.0.0.0:5451->5432/tcp   hasura-multi-schema_pg_1_1
7b9b042e2404        postgres:12                    "docker-entrypoint.s…"   29 seconds ago      Up 28 seconds       0.0.0.0:5452->5432/tcp   hasura-multi-schema_pg_2_1
```