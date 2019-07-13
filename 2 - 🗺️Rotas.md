# 🗺️Rotas

**🔎O que são?**

Rotas irão configurar o que deve ser visualizado ao acessar determinados caminhos na URL do domínio.

**📌Onde estão?**

As rotas podem ser acessadas e modificadas através do caminho:

```php
routes/web.php
```

**🏳️ Definições práticas**

O método mais simples de se criar uma nova rota é através de:

```php
Route::get('/rota', function () {
    return view('pasta.index');
});
```

Outro método mais complexo é importar todas as rotas de um controlador, cujo irá definir novas rotas baseando nas funções do controlador.

```php
Route::resource('nomeDaRota','controlador');
```

**👀 Visualizando rotas**

É possível visualizar todas as rotas da aplicação através do comando no console

```
php artisan route:list
```

```
+--------+----------+----------+------+---------+--------------+
| Domain | Method   | URI      | Name | Action  | Middleware   |
+--------+----------+----------+------+---------+--------------+
|        | GET|HEAD | /        |      | Closure | web          |
|        | GET|HEAD | api/user |      | Closure | api,auth:api |
+--------+----------+----------+------+---------+--------------+
```

