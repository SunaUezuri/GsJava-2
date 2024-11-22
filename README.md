# EcoGenius 🌱

**EcoGenius** é uma plataforma digital inovadora desenvolvida para educar, engajar e conectar usuários, empresas e organizações na transição para práticas mais sustentáveis e uso de energias renováveis. Criada pela startup **CadeGenius**, a iniciativa busca promover uma economia de baixo carbono, democratizar o acesso a soluções ecológicas e incentivar ações práticas em prol de um futuro mais sustentável.

## 🌟 Visão Geral do Negócio

A EcoGenius é a segunda iniciativa da **CadeGenius**, uma startup sem fins lucrativos fundada em 2024 com a missão de conscientizar sobre questões ambientais e acelerar práticas sustentáveis por meio da transformação digital. A plataforma:
- **Promove a redução de emissões de gases de efeito estufa.**
- **Conecta consumidores e empresas eco-responsáveis.**
- **Oferece conteúdo educativo sobre economia circular e energias renováveis.**

Em um contexto onde o Brasil enfrenta desafios ambientais significativos, como a geração de 79 milhões de toneladas de resíduos sólidos anualmente, a EcoGenius surge como uma resposta prática e inovadora.

## 🌍 Funcionalidades Principais

1. **Área de Ideias** 💡  
   Um espaço colaborativo para os usuários proporem soluções inovadoras e práticas voltadas à sustentabilidade, como:
   - Incentivo ao uso de energias limpas.
   - Redução da pegada ecológica.
   - Engajamento em uma cultura de co-criação.

3. **Biblioteca de Energia Limpa 📚**  
   Uma central de informações sobre diferentes fontes de energia renovável (solar, eólica, biomassa etc.), com dados atualizados para desmistificar essas tecnologias.

4. **Fórum de Discussão 🗨️**  
   Um espaço interativo para compartilhar experiências, discutir desafios ambientais e trocar ideias sobre práticas sustentáveis.

5. **Dicas e Receitas Sustentáveis 🌱**  
   Sugestões práticas para reduzir o impacto ambiental, como receitas de produtos de limpeza ecológicos, compostagem e economia de recursos.

6. **Rede de Empresas Sustentáveis 🏢**  
   Diretório de empresas certificadas que adotam práticas ecológicas, detalhando suas iniciativas em economia circular, fontes de energia limpa e metas de redução de emissões.

7. **Monitoramento e Feedback 📊**  
   Ferramenta para que os usuários acompanhem o impacto de suas ações e escolhas sustentáveis.

## 🛠️ Tecnologias Utilizadas

- **Java**: Linguagem principal do projeto.
- **Maven**: Gerenciador de dependências.
- **Banco de Dados Oracle**: Utilizado para armazenar informações.

## 📂 Estrutura do Projeto

- **`pom.xml`**: Configuração do Maven e gerenciamento de dependências.
- **`script.sql`**: Scripts de criação de tabelas para o banco de dados.
- **`equipe.txt`**: Informações sobre a equipe de desenvolvimento.
- **`Camada Model`**: É onde estão todas as classes principais do projeto, classes que estarão representando as tabelas do banco de dados, além de classes ENUM para denominar certos atributos, é nessa camada que está a a base do projeto e servirá de estrutura para o resto dele.
- **`Camada Factory`**: Camada que contém uma classe única, ela é a responsável por fazer a conexão com o banco de dados da aplicação, nela estão os dados necessários para o acesso e utilização das classes da próxima camada
- **`Camada Exception`**: Nessa camada é onde tratamos alguns dos erros que podem ocorrer na aplicação, como a Exception IdNaoEncontradoExption, que envia uma mensagem sempre que o ID inserido não é encontrado no banco de dados.
- **`Camada DAO`**: Esse é o corpo do projeto, é nela onde estão as classes que serão responsáveis por realizar as operações junto ao banco de dados, nelas temos desde funções comuns para todas como:

INSERT_SQL
UPDATE_SQL
SELECT_ALL_SQL
SELECT_BY_ID_SQL
DELETE_SQLQ

Até selects mais específicos como:

SELECT_BY_EMAIL_SQL.

- **`Camada DTO`**: Nessa camada contém as regras de negócio da aplicação, é nela que estão definidas por exemplo oq será mostrado nos SELECTS, o quanto de caracteres máximos algum atributo pode ter ao se cadastrar, se algum atributo é obrigatório ou não para o cadastro e entre outros, é uma camada que se juntará a próxima para finalizar a aplicação.
-**`Camada Resource`**: É a camada responsável por criar a API em si, é nela que foram feitos os métodos HTTP de todas as classes da model, ela utiliza diretamente tanto a DTO quanto a DAO para fazer as operações mais seguras e funcionais, ela é a responsável também por exibir tudo no front-end sendo o passo final para a aplicação.

## 🚀 Como Usar

1. **Clone o repositório**:
   ```bash
   git clone <url-do-repositorio>

**IMPORTANTE:**
**Há uma chance de ao fazer o clone o programa não funcionar corretamente devido ao plugin do Lombok que por algum motivo ao ser enviado ao Github e depois ser clonado o programa não reconhece mais o Lombok, caso isso ocorra instale o zip do projeto no mesmo local onde você consegue a URL.**

2. **Ferramenta**:
3. 
   Recomenda-se o uso do IntelliJ pois ele pode fornecer todas as funcionalidade e dependências necessárias sem chances de haver algum erro grave.

4. **Dependências**:

   No IntelliJ tenha certeza de ter instalado a extensão do Lombok pois ela é fundamental para o funcionamento do sistema.

   "Onde Baixar?"

   Vá em File > Settings > Plugins

   Então clique em MarketPlace e pesquise "Lombok"

   Instale o plugin e clique em "apply" e depois em "ok"
   
![Captura de tela 2024-11-22 093400](https://github.com/user-attachments/assets/8490c6a3-a609-46d1-84d3-03aa7d7f9634)

4. **Como rodar**:

   Dentro da pasta src haverá o que chamamos de package com o nome "br.com.fiap.ecogenius", nele haverá outros pacotes que representam as camadas mencionadas anteriormente e um arquivo separado chamado "Main".

   Para rodar o programa basta clicar nesse arquivo Main e clicar no botão verde de play.
  
![Captura de tela 2024-11-22 094042](https://github.com/user-attachments/assets/088f7ad6-ba32-416f-bcc0-eb66ee4cdcd0)
