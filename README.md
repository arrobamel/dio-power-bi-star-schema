![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Star Schema](https://img.shields.io/badge/Feito%20com-Star%20Schema-blue?style=for-the-badge)
![DIO](https://img.shields.io/badge/DIO-Bootcamp-red?style=for-the-badge)

# Meu Projeto Star Schema - DIO

Eu peguei a tabela Financial Sample que era tudo em uma tabela só e transformei no modelo estrela que a professora pediu no desafio.

### O que eu fiz:

**1. Backup**
Dupliquei a original pra `Financials_origem` e ocultei pra não perder nada.

**2. D_Produtos**
Usei **Agrupar por** em cima de `Product` e calculei média de unidades, média de venda, mediana, máximo e mínimo como pedido. Depois criei **Coluna de Índice de 0** e virou meu `ID_Produto`.

**3. D_Descontos e D_Detalhes**
Fiz por **Referência** + **Remover Duplicatas** pra pegar só os valores únicos de `Discount Band`, `Segment`, `Country`.

**4. D_Calendario**
Fiz por DAX:
```DAX
D_Calendario = CALENDAR(DATE(2013,1,1), DATE(2014,12,31))
