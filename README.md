## 🚀 Cypress Discovery 🚀

Projeto de estudo sobre [Cypress](https://www.cypress.io/). O material disponível neste repositório foi desenvolvido durante o curso cypress discovery, disponibilizado pela [QA ninja](https://app.weareqacademy.com).

O objetivo deste projeto é compreender o funcionamento do cypress aplicado a um caso real. Para tanto, foi utilizado o [buger eats](https://buger-eats-qa.vercel.app) como objeto de testes. 

Os testes criados analisaram a adição de um novo usuário à plataforma e validação de formulários. Além disso, foi utilizado o padrão PageObject para estruturar os testes.


### 💡 Conceitos abordados
-----------------------

- Checkpoints na Automação Web;
- CSS Selector;
- Evidências de testes em vídeo;
- Ganchos (after, after each, before e before each)
- Massa de testes estática (*.json) e dinâmica ([faker](https://www.npmjs.com/package/@faker-js/faker))
- Padrão PageObject;
- Screenshots quando um teste falha;
- Submeter forms e validar modal;
- Upload de arquivos;


### ⚠️ Instalação e uso do projeto
-----------------------

- Instale o [Node.js](https://nodejs.org/en/download/);
- Abra o diretório do projeto e execute o comando:
    - `npm install`
    - `npm install faker@5.5.3 --save-dev` (para instalar a biblioteca Faker)
    - `npm install cypress-file-upload --save-dev` (para instalar o file-upload)
- Para abrir a interface de execução do Cypress, execute no diretório do projeto:
    - `npx cypress open`


### ⚙️ Arquitetura do projeto
-----------------------

```
cypress-discovery/
  ├─  cypress/
  │        ├── factories/
  │        │   └── *.js
  │        │
  │        ├── fixtures/
  │        │   └── images/
  │        │       └── *.png    
  │        │
  │        ├── integration/
  │        │   ├── cadastro.spec.js
  │        │   └── home.spec.js
  │        │
  │        ├── pages/
  │        │   └── SignupPage.js
  │        │
  │        ├── plugins/
  │        │   └── index.js
  │        │
  │        └── support/
  │            ├── Commands.js
  │            └── index.js
  │ 
  ├── node_modules/
  ├── cypress.json
  ├── package-lock.json
  ├── package.json
  └── README.md
```

## 🔍 Camadas do projeto
---------------------------------------

 - **factories:** arquivos para massa de dados dinâmicas para os testes (*.js);
    - **images:** arquivos para upload nos formulários (*.jpg);
 - **integration:** arquivos de testes separados em categorias a organização (*.spec.js);
 - **pages:** arquivos com as páginas de funcionalidades dos testes (*.js);
 - **plugins:** plugins que são utilizados na solução ficam dentro do arquivo "plugins/index.js";
 - **support:** camada com comandos Cypress customizados e sobrescritas globais:
    - Arquivo commands.js responsável de receber os comandos globais no cypress;
    - Arquivo index.js responsável de receber as importações dos comandos cypress;
 - **node_modules:** arquivos ou diretórios que podem ser carregados pelo Node.js;
 - **cypress.json:** arquivo de configuração do Cypress;
 - **package-lock.json:** gerado automaticamente com as instalações e atualizações de pacotes;


