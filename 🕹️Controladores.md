# 🕹️Controladores

**🔎O que são?**

Controladores basicamente auxiliam na gestão de rotas da aplicação. Ele também irá trabalhar no auxílio do repasse de informações do banco de dados, para páginas estáticas. 

*Palavras chave: gestão de rotas, repasse de informações do banco de dados*

**📌Onde estão?**

Os controladores ficam na seguinte pasta do projeto:

```
.\app\Http\Controllers
```

**⚙️Como configurá-los?**

Todos controladores irão possuir funções como essa:

```php
public function index()
{
    return view('home.index');
}
```

Cujo irão retornar a renderização de alguma página. No exemplo acima, está retornando a página index, na pasta home, localizada dentro da pasta Views do projeto. Cada função em um controlador será responsável por uma rota diferente.

**➕ Criando novos controladores**

Para criar um novo controlador pode se utilizar o comando a seguir, cujo irá definir também rotas básicas de manuseio da aplicação, em função do argumento `--resource`:

```php
php artisan make:controller Nome --resource
```



