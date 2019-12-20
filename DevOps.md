# DevOps Essential  
 
========================= 
# A Cultura DevOps 
========================= 

## Sobre o curso (4Linux)  

DevOps é uma filosofia que tem como principal objetivo a união dos times de TI em prol de uma entrega de serviços com maior qualidade e rapidez  
 
O curso tem por objetivo introduzir o amplo mercado que está cada dia mais forte  

## O que é DevOps?   
- DevOps surgiu da comunidade;  

- Não há por trás empresa ou organização que regulamente;  

> _É a combinação de filosofias culturas, práticas e ferramentas para que exista um alinhamento dos times de Desenvolvimento e Operação com foco na entrega na entrega rápida de serviços com alto grau de qualidade_  

- Tem como princípio promover a união entre as áreas e TI  

## Acontecimento que levaram ao surgimento do DevOps  
- 2001 Surgimento do Ágil;  

    - Desruptura da metodologia de desenvolvimento - entregas rápidas, mas havia um gargalo no time de operações;  

- 2003 Google fez a reestruturação da área de infraestrutura - movimento em que um engenheiro de software passa a gerenciar o time de operações, de modo que o gerenciamento fosse semelhante ao desenvolvimento; porém a publicação com os melhores resultado obtidos foi feita apenas em 2016;  

- 2005 surgimento de Git (gerenciamento de versão) e Puppet (Gerenciamento de configuração)  

- 2009 Velocity e DevOps - impulsionaram a consolidação. Também surge a ferramenta Chef.  

- 2012 surge a ferramenta Ansible  

- 2013 é lançado o Livro _The Phoenix Project_  

## Pilares  

-  **CULTURA**  

Promoção da união dos times - **desenvolvimento e TI trabalhando juntos** -, de modo que todos trabalham de forma **colaborativa**;   
- **AUTOMAÇÃO**  

Para que as entregas sejam feitas de maneira rápida, é preciso que as etapas estejam automatizadas;  

- **MEDIÇÃO**  

Premissa que considera que tudo tem de ser medido e monitorado para que tenhamos dados concretos para embasar possíveis melhorias.   
- **COMPARTILHAMENTO**  

Como todos estão trabalhando para convergir para um mesmo resultado as **responsabilidades devem ser compartilhadas** e deve sempre ocorrer **feedback em todas as fases**  

## Características  
 
- Desenvolvimento utilizando metodologias ágeis, para entrega rápida  

- Software buscando baixa acoplação, mirando a estrutura de microservices;  

- CI/CD  

- Infraestrutura com gerência de configuração  

- Centralização de logs e disponibilização dos logs para todos os times  

- Adaptar o desenvolvimento de software seja adaptado ao desenvolvimento de infraestrutura;  

## Benefícios   

- Melhor comunicação e maior colaboração entre os times Dev. e Ops  

- Redução nas falhas na implantação de mudanças  

========================= 
# Pipeline DevOps 
========================= 
## Terminologias 

**Infraestrutura Ágil**: é a infraestrutura automatizada, quando usamos ferramentas de configuração, virtualização, cloud, etc., indo na direção de uma infraestrutura em que menos é necessário o acesso manual aos usuários; 

**Infraestrutura como Código (IaC)**: É pensar na criação de infraestrutura com ciclo de via vida semelhante ao desenvolvimento de software; 

**Gerência e Configuração**: Ferramentas para permitir que haja infraestrutura como ágil, é a aplicação da infraestrutura como Código; 

**Provisionamento**: automatização do provisionamento de máquinas;  

**Desenvolvimento Ágil**: possui entrega menores; 

**Integração Contínua**: o código criado/alterado deve ser integrado ao projeto principal, de modo que seja verificado se o mesmo não gerou alguma inconsistência ou bug no projeto;  

**Entrega Contínua**: feitos os testes de aceitação e preparações para eu o código esteja apto a ir para o ambiente de produção; o deploy não é automático, mas deve ser automatizado; 

**Implantação Contínua**: Dado o momento que o Dev. Acredita que o código está pronto, então ele promove o código pra que passe por todos os testes até ser entregue no ambiente de Produção, automaticamente. 

## Pipeline de Desenvolvimento 

**OBJETIVO** 

Entregar releases de softwares confiáveis de forma automatizada; 

![Pipeline de Desenvolvimento](C:\Users\andressa.farias\Pictures\img-git) 

## Pipeline DevOps 

É um agregado de pipelines 
A pipeline deve ser moldada de acordo com a maturidade da empresa, necessidade e automação  

![Evolução Pipeline](C:\Users\andressa.farias\Pictures\img-git) 

========================= 
# Certificações 
========================= 

- It.cert 
- EXIN Brail - https://www.exin.com/br-pt/certificacoes/#qualification-program/exin-devops 
- LPI - https://www.lpi.org/pt/our-certifications/devops-overview 

========================= 
# Laboratório DevOps  
========================= 

## Ferramentas 
- GitHub 
- CodAnyhere 
- Trave CI 
- Hiroku 

## Passos
1. **Criar repositório de Documentação**
- Criar no GitHub um novo repositório;
- Marcar ele como público;
- Marcara criar arquivo de Readme.md;
- Escolher uma licença.

Para controle as trefas pode ser usado o próprio Git, para isso no Repositório de documentações, executar os passos
- Clicar em _Project_
- _Create Project_
- Preencher as infomações e selecionar o template _Kanbam _(Basic)_
- _Create Project_

2. **Criar uma aplicação**

Para fins de facilitar iremos apenas editar uma aplicação já existente
- Buscar o github da 4linux
- Na págna de retorno Clicar em _Users_
- Clicar no perfil na 4Linux
- Clicar em Repositório
- Acessar o repoitório _DevOpsLab-HelloWorld_
- Fazer um _Fork_ do repositório - após a cópi finalizada, voltamos automaticamente ao nosso repositório no GitHub que possui o mesmo nome do repositório clonado.

3. **Conectar a IDE ao repoitório**
- Acessar a IDE _codeanywhere_
- File \> New Connection \> GitHub
- Se o repositório  não for clonado automticmente é possivel fazer o clone do repositório: git clone https://github.com/AndressaFarias/DevOpsLab-HelloWorld.git
-  selecionar a stack python

4. **Alterar a aplicação**
- Acessar a pasta _template_ e abrir o arquivo _index.html_
- Alterar o campo de cabeçalho para um mensagem qualquer [linhas 13].
- Fechar o arquivo editado
- Clicar emcima da pasta do projeto e clicar em _SSH Terminal_
- Executar o comando _git status_
- Executar o comando _git add --all_, para adicionr todos os aruivo alterados ao _commit_
- Executar o comando _git commit -m "Log"_
- Executar o comando _git push origin master_, para subir as alterações pra o GitHub.
- Inserir as credencias de login no Git

5. **Configurar o processo de _Build_**

A proxima etapa é a de configuração _Trevis CI_ como sendo o processo de Integrção Contínua.
- Se a conta no Travis foi criada vinculada conta do GitHub então é só clicar no botão de _Sync Account_ 
- Ativar  projecto que será utilizado;
- Clicar no nome do projeto;
- Clicar em _Settings_  e verificar se a opção _Build puhe branches_ está ativa, essa opção faz com que a cada push realizado será feito o _build_
- Clicar no botão do status da compilação "build unknown", alterar o campo _Format_ para _Markdown_ e copiar o contúdo do campo _Result_ para que possamo iserir a flag de status da compilação no GitHub. Para isso executamo os seguinte passos:
    - Acessar a IDE _codeanywhere_ 
    - Abrir o arquivo _Readme.md_ e alterar a linha 4 para o conteudo copiado Travis;

Para usarmos o Travis como ferramenta de CI precisamos ter dentro do nosso repositório do GitHub arquivo _.travis.yml_ 

Como alteramo o arquivo _Readme_ precisamos fazer o commit dessa alteração, então executamos o seguintes passos:
- Na IDE codeanywhere abrimos um terminal SSH;
- Devemos fazer o _commit_ das alterações: _git add ._ e _git commit -m Update Readme"_

Essa atualização também será refletida no Traveis, pois a integração já foi feita;  

Ao consultar no GitHub veremos a alteração que foi feita o _commit_

Ao consultar o Travis veremos que o nosso projeto estará com sinaliação _"amarela"_, pois identificou a existencia de um _build_. 

Ese build irá falhar, pois o teste de conteúdo irá falhar. Para corrigir o erro reportado devemos seuir os seguintes comandos:
- Acessar a IDE
- Ir até o arquivo de teste _test.py_
- Na linha referente ao teste de conteúdo altera  contúdo, pa o mesmo que foi inserido no Index.html
- Fazer commit e push
- No Travis podemo ver que será feito um novo _build_ 

6. **Deploy e Operações**
Usaremos o Herou como sendo nosso ambiente de produção
-  Acessar o Heroku
- Copiar a _API KEY_ para integrá-lo ao Travis-CI
    - Clicar em _Create new app_
    - Criar um _App name_ único
    - Clicar na foto do user
    - Clicar em _Account settings_
    - Copiar o conteúdo do campo _API KEY_
- Voltar ao Travis
- Clicar _settings_ do projeto 
- No campo Environment Variable criar uma variavel de ambiente e inseir o valor da chave copiada no heroku; Essa variavel deve estar declarada dentro do arquivo _.travis.yml_
- Alterar no arquivo _.travis.yml_ o nome da app, dentro do bloco de _deploy_ , eve ser o memso nome da aplicação crida no Heroku.