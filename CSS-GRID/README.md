# CSS GRID layout
## Font's
1 - [origamid](origamid.com/)

___

## Grid Container
````
    O Grid Container é a tag que envolve os itens do grid,
ao indicar display: grid, essa tag passa a ser um Grid Container.
````

## Principal elemento - Display
 - Torna o elemento um grid container.
````
display: grid;
````
___
## Secundário elemento - grid-template-columns
 - Define o número total de colunas que serão criadas no grid.


Quatro colunas contento 100px de largura são criadas.
````
grid-template-columns: 100px 100px 100px 100px;
````

Duas colunas são criadas, sendo a segunda com o dobro do tamanho da primeira. fr é uma unidade fracional. O tamanho do conteúdo é respeitado, ou seja, se o conteúdo na primeira coluna for maior que o da segunda, a primeira será maior.
````
grid-template-columns: 1fr 2fr;
````

Três colunas são criadas, a primeira terá no mínimo 200px de largura e no máximo 1fr(isso significa que após 200px ela se expande da mesma forma que as outras colunas). As outras duas colunas vão ter 1fr.
````
grid-template-columns: minmax(200px, 1fr) 1fr 1fr;
````

Cria 3 colunas com 1fr de tamanho. O repeat seria a mesma coisa que escrever 1fr 1fr 1fr
````
grid-template-columns: repeat(3, 1fr);
````

Cria automaticamente um total de colunas que acomode itens com no mínimo 100px de largura.
````
grid-template-columns: repeat(auto-fit, minmax(100px, auto));
````
___