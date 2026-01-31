## 🧪 QA Portfólio - API Rosário Católico (rosariumrest) ✝

### API REST desenvolvida para fornecer dados do Rosário Católico.

### 🔗 API em produção (Vercel):

<a href="https://rosariumrest.vercel.app/day-mysteries" target="_blank"  rel="noopener noreferrer">https://rosariumrest.vercel.app/day-mysteries</a>

## 📖 Dados gerais da API:

#### Esta API foi desenvolvida por <a href="https://www.github.com/AurinoMSMF" target="_blank"  rel="noopener noreferrer">mim mesmo</a> e possui apenas rotas GET, por se tratar de um domínio de leitura, sem necessidade de operações de escrita.. Os endpoints funcionais são:

### `GET /day-mysteries`

- #### Retorna o tipo dos mistérios e os mistérios correspondentes ao dia atual em latim. Ex.: Se o dia for segunda-feira, os mistérios retornados são do tipo mysteriaGaudiosa (Mistérios Gozosos).

### `GET /day-mysteries/{day}`

- #### Retorna o tipo dos mistérios e os mistérios do dia fornecido. O parâmetro `/{day}` pode ser uma string contendo o nome do dia em inglês ou o número do dia na seguinte ordem: 1 - Domingo e 7 - Sábado.

## 🔎 Escopo dos testes

### Os testes foram realizados sobre os endpoints da API, considerando:

- #### Respostas HTTP
- #### Estrutura do payload
- #### Regras de negócio

## 🧪 Tipos de teste aplicados

- #### Smoke test (endpoints principais)
- #### Testes funcionais de API

## 🔬 Casos de teste

- #### [Acessar casos de teste](test-cases/test-cases.md)

- #### Cada caso segue um padrão contendo:
  - ##### ID - Título
    - ###### Endpoint(s) testado(s)
    - ###### Pré-condição
    - ###### Passos (steps)
    - ###### Resultado esperado
    - ###### Resultado obtido
    - ###### Status

## 🐞 Relatórios de bug (Bug reports)

- #### [Acessar bug reports](bug-reports/)

- #### Cada bug report segue um padrão contendo:
  - ##### Identificação
  - ##### Caso de teste relacionado
  - ##### Descrição
  - ##### Passos para reprodução
  - ##### Resultado esperado
  - ##### Resultado obtido
  - ##### Severidade
  - ##### Prioridade

## 🧠 Aprendizados

- #### Escrita de casos de teste para APIs REST
- #### Testes de API via Postman
- #### Documentação clara com bug reports
- #### Importância da validação de regras de negócio

## 🔨 Ferramentas utilizadas

- #### Postman 👨‍🚀 — execução de smoke tests e testes funcionais de API

### 📚 Organização dos testes no Postman 👨‍🚀

- #### A collection do Postman foi organizada em pastas por tipo de teste (smoke e funcionais), mantendo rastreabilidade com os casos de teste documentados.

![Estrutura de testes no Postman](postman/postman-full-organization.png)

- #### 📦 [Collection do Postman em JSON](postman/tests-rosariumrest.postman_collection.json)
