# OpenAPI

## Goal

1. Split API definition.
2. Externalize API definition(s).

## TL;DR

1. Remove all files in [`swagger`](swagger) directory.
2. Copy your API definition with OpenAPI format.
    - Use [`swagger/api.yaml`](swagger/api.yaml) file.
    - Split definition with `$ref`, like [`paths./pet.$ref`](swagger/api.yaml#L35) -> [`pet`](swagger/pet.api.yaml#L1)
3. Run container.
    ```shell
    cd open-api-workflow
    docker compose up -d
    ```
4. Edit API definition with your IDE.