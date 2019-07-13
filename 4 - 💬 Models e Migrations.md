# 💬 Models e Migrations

Models irão auxiliar na comunicação com o banco de dados. E migrations irão auxiliar no repasse de bancos de dados para SQL, além da definição de novas colunas no banco de dados.

**⚙️Configurando banco de dados local**

Acesse o arquivo:

```
.env
```

Substitua as linhas:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=
```

**➕ Criando novos modelos**

Para criar um novo modelo é possível através do comando, cujo irá tambem criar uma interface de migração do banco de dados.

```
php artisan make:model nome -m
php artisan migrate
```

**🏷️ Alterando colunas**

Para alterar as entradas que esse modelo terá no banco de dados, vá ate:

````
./database/migrations
````

E altere a função up():

````php
public function up()
{
	Schema::create('salves', function (Blueprint $table) {
	$table->bigIncrements('id');
	$table->timestamps();
	});
}
````

