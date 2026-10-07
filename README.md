[Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
[Star Schema](https://img.shields.io/badge/Modelagem-Star%20Schema-0078D4?style=for-the-badge)
[DIO](https://img.shields.io/badge/Bootcamp-DIO-EC0000?style=for-the-badge)

# Meu Projeto Star Schema - DIO

> Eu peguei a tabela Financial Sample que era tudo em uma tabela só e transformei no modelo estrela que a professora pediu no desafio.

### 🧠 O que eu fiz:

**1. Backup**
Dupliquei a original pra Financials_origem e ocultei pra não perder nada.

**2. D_Produtos**
Usei Agrupar por em cima de Product e calculei média de unidades, média de venda, mediana, máximo e mínimo como pedido. Depois criei Coluna de Índice de 0 e virou meu ID_Produto.

**3. D_Descontos e D_Detalhes**
Fiz por Referência + Remover Duplicatas pra pegar só os valores únicos de Discount Band, Segment, Country.

**4. D_Calendario**
Fiz por DAX: D_Calendario = CALENDAR(DATE(2013,1,1), DATE(2014,12,31))

**5. F_Vendas**
A parte mais importante. Usei Mesclar Consultas pra trazer os IDs das dimensões. E depois apaguei tudo que era texto (Product, Segment, Month Name) porque na fato só pode ficar número e ID. Se deixar texto fica duplicado.

**6. Modelo**
Liguei no modelo 1 para muitos de cada dimensão pra F_Vendas e ficou a estrelinha.

### 🖼️ Meu modelo final
<img width="863" height="557" alt="diagramastar" src="https://github.com/user-attachments/assets/dd246852-4a1b-4ff3-8605-d424ea255c05" />



### 🛠️ Tecnologias
- Power Query (Agrupar, Índice, Mesclar, Remover Duplicatas)
- DAX (CALENDAR)
- Modelagem Star Schema
