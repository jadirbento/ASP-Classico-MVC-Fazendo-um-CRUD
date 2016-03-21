# ASP Clássico MVC (fazendo um CRUD)

[![ASP-Clássico-MVC](http://pilaronline.net/namiinfo/wp-content/uploads/2012/01/logo_asp.png)](http://pilaronline.net/namiinfo/wp-content/uploads/2012/01/logo_asp.png)

ASP-Clássico-MVC é um modelo de desenvolvimento baseado em ASP.NET MVC4, que pode ser bem interessante para aqueles que gostam de separar o código do HTML.

O ASP Clássico não é capaz de aproveitar cem por cento dos benefícios do MVC, entretanto, com este modelo podemos organizar bem o nosso código separando as camadas e suas responsabilidades, ganhando assim em produtividade e desempenho.


## RouteConfig
```
http://localhost/?grupos/index/
http://localhost/?grupos/cadastrar/
http://localhost/?grupos/atualizar/4/
http://localhost/?grupos/excluir/4/

```
Estas requisições acimas são resolvidas pelo RouteConfig da seguinte forma:

-O primeiro parâmetro é o `Controller` (controller=grupos);

-O segundo parâmetro é uma `Action` (action=cadastrar);

-O terceiro parâmetro é um `ID`, é obrigatório se a requisição for diferente de index.


Outros parâmetros também pedem ser passados, por exemplos:
`http://localhost/?grupos/detalhes/2/partial:view/`.

Esta requisição retorna um conteúdo simples (sem menu, por exemplo), isso você define no layout do 
ajax. Neste mesmo formato você pode informar por exemplo, a paginação etc.

Os parâmetros são passados e recebidos da seguinte forma:

```
Public Sub Excluir(vars)
    Dim res, objEx
    Set objEx = new GruposHelper
    res = objEx.Excluir( vars("id") )
    If res = false Then
        'erro
    Else
        'sucesso
    End If
End Sub
```





## Models




## Controllers


# Views

