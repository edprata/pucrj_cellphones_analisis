# MVP Análise de Dados e Boas Práticas

Projeto final da disciplina Análise de Dados e Boas Práticas do MBA PUC-RJ em Ciências de Dados.

**Nome:** Edmilson Prata da Silva

**Matrícula:** 4052024002125

**Dataset:** Mobiles Dataset (2025): Modelos de Celulares lançados entre 2015 e 2025 ([fonte](https://www.kaggle.com/datasets/abdulmalik1518/mobiles-dataset-2025/data)).

**Versão Google Colab:** https://colab.research.google.com/drive/1COYP7EiCyJfOa3fxHhRpWXa26XWZJoRQ?usp=sharing


## Contextualização

### 1. Descrição do Problema

O objetivo deste trabalho é responder a questionamentos de negócio para uma empresa que deseja iniciar no ramo de fabricação de aparelhos celulares. A empresa pretende entrar no mercado com 3 classes de aparelhos:

1. Classe de entrada: Aparelhos mais baratos e com recursos de hardware mais modestos;
2. Classe intermediária: Aparelhos de valor intermediário e mais recursos que a classe de entrada;
3. Classe especial: Aparelhos mais caros e mais robustos em termos de hardware.

A empresa deseja também obter insights sobre este ramo de atividade e, desta forma, definir as características para o lançamento de produtos com maior potencial de venda e lucratividade, acompanhando as tendências de mercado.

Para tanto, uma base de dados pública, a ser detalhada mais à frente, foi escolhida para responder às questões de negócio (hipóteses) levantadas pela equipe do projeto.

Ao final, pretende-se criar um modelo de ML que, de acordo com as características de um possível novo modelo de celular apresentado (em tempo de projeto), indique em qual das três classes de produtos o modelo melhor se enquadra.


### 2. Hipóteses do Problema

As hipóteses traçadas são as seguintes:

a) Quais características técnicas dos aparelhos são mais relevantes para lançamento de novos modelos?

É preciso descobrir quais são as configurações mais relevantes do ponto de vista do lançamento de novos produtos. Com isso, pode-se descobrir quais são as características técnicas mais recomendadas para o lançamento de novos produtos no mercado, com potencial de concorrer com os modelos de fabricantes já conhecidos. Isso pode evitar que novos produtos sejam lançados pela empresa estando muito distantes da realidade do mercado, em comparação a modelos existes e, dessa forma, provocar má aceitação dos produtos.

b) Quais as faixas de preço praticadas pelo mercado?

É importante saber quais as faixas de valores dos modelos existentes, de acordo com suas características técnicas, para definir a política de preços de novos produtos. Com isso, pode-se estabelecer preços de lançamentos compatíveis com o mercado e evitar um distanciamento da política de preços praticada pelos concorrentes.


### 3. Tipo de Problema

Este é um problema de classificação supervisionada. Dado um conjunto de características, inerentes a um possível novo modelo de celular, o objetivo é dizer em qual classe de produtos (já apresentadas) o modelo melhor se enquadra.


### 4. Seleção de Dados

#### 4.1. Fonte de dados

A fonte de dados utilizada foi obtida no site Kaggle ([link](https://www.kaggle.com/)), que é bastante conhecido por profissionais das áreas de Data Science e Analytics. Este site oferece bases de dados de todos os tipos de temas, de dados científicos a dados para negócios. É uma base comunitária bastante respeitada e que oferece dados de qualidade de todo o mundo.

O conjunto de dados utilizado para este trabalho ([link](https://www.kaggle.com/datasets/abdulmalik1518/mobiles-dataset-2025/data)), segundo a descrição e detalhamento contido no próprio site Kaggle, segue conforme citação a seguir, em versão traduzida do original, em inglês:

“Este conjunto de dados contém especificações detalhadas e preços oficiais de lançamento de vários modelos de celulares de diferentes empresas. Ele fornece insights sobre hardware de smartphones, tendências de preços e competitividade de marcas em vários países. O conjunto de dados inclui recursos importantes como RAM, especificações da câmera, capacidade da bateria, detalhes do processador e tamanho da tela.”

A documentação ressalta que um aspecto importante do conjunto de dados são as informações de preços. Estes preços, na verdade, são os preços oficiais de lançamento dos aparelhos celulares. Para esta pesquisa, utilizaremos o valor em dólar, apesar do conjunto de dados conter preços de alguns outros países. Estes preços podem oferecer insights valiosos sobre tendências de mercado e, devido a esta característica, a base foi escolhida para apoiar este trabalho de pesquisa.


#### 4.2. Features da fonte de dados

Nesta seção serão detalhados os campos, ou features, do conjunto de dados obtido no site do Kaggle para a realização do trabalho desta pesquisa, conforme segue:

1. Company Name: A marca ou fabricante do telefone celular.
2. Model Name: O modelo específico do smartphone.
3. Mobile Weight: O peso do celular (em gramas).
4. RAM: A quantidade de memória de acesso aleatório (RAM) no dispositivo (em GB).
5. Front Camera: A resolução da câmera frontal (selfie) (em MP).
6. Back Camera: A resolução da câmera traseira principal (em MP).
7. Processor: O chipset ou processador usado no dispositivo.
8. Battery Caoacity: O tamanho da bateria do smartphone (em mAh).
9. Screen Size: O tamanho da tela do smartphone (em polegadas).
10. Launche Price (Paquistão, Índia, China, EUA, Dubai): O preço oficial de lançamento do celular no respectivo país no momento de seu lançamento. Os preços variam de acordo com o ano em que o celular foi lançado.
11. Lauched Year: O ano em que o celular foi lançado oficialmente.
