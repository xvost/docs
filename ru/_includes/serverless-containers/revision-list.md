{% list tabs %}

- Консоль управления

    1. В [консоли управления]({{ link-console-main }}) перейдите в каталог, в котором находится контейнер.
    1. Выберите сервис **{{ serverless-containers-name }}**.
    1. Выберите контейнер, для которого хотите получить список ревизий.
    1. В разделе **Ревизии** будет показан список ревизий контейнера и подробная информация о них.

- CLI

    {% include [cli-install](../cli-install.md) %}

    {% include [default-catalogue](../default-catalogue.md) %}

    {% include [note](./sc-list-note.md) %}

    Чтобы получить список ревизий контейнера, выполните команду:

    ```
    yc serverless container revision list --container-name <имя_контейнера>
    ```

    Результат:

    ```
    +----------------------+----------------------+--------------------------------------------+---------------------+
    |          ID          |     CONTAINER ID     |                   IMAGE                    |     CREATED AT      |
    +----------------------+----------------------+--------------------------------------------+---------------------+
    | bbaq84v92qqc******** | bbab5i36nvda******** | {{ registry }}/crpp35hht729********/ubuntu:test | 2021-09-09 11:22:28 |
    | bba5eosk5sod******** | bbab5i36nvda******** | {{ registry }}/crpp35hht729********/ubuntu:test | 2021-09-09 10:13:04 |
    +----------------------+----------------------+--------------------------------------------+---------------------+
    ```

- API

  Чтобы получить список ревизий контейнера, воспользуйтесь методом REST API [listRevisions](../../serverless-containers/containers/api-ref/Container/listRevisions.md) для ресурса [Container](../../serverless-containers/containers/api-ref/Container/index.md) или вызовом gRPC API [ContainerService/ListRevisions](../../serverless-containers/containers/api-ref/grpc/container_service.md#ListRevisions).

{% endlist %}