Copie sua chave SSH:

    ssh-copy-id root@<host>

Preparar o ambiente:

    bundle exec knife solo prepare root@<host>

Isso além de instalar o chef no ambiente remoto, criará um arquivo ``nodes/seuipdoserver.json``.
Substitua o conteúdo desse arquivo com o conteúdo do arquivo ``nodes/rails_postgres_redis.json.example``.

Instalar as dependências no server:

    bundle exec knife solo cook root@<host>
