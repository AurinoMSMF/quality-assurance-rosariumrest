## 🧪 CT-00 — Smoke test dos endpoints principais

### Endpoints:

- `GET /day-mysteries`

- `GET /day-mysteries/{day}`

### Pré-condição:

- API disponível

### Passos

- Executar `GET /day-mysteries`

- Executar `GET /day-mysteries/monday`

### Resultado esperado:

- Ambos retornam status code 200

- API funcional para testes mais aprofundados

### Resultado obtido:

- Status code 200 em ambos os endpoints
- API disponível para testes

### Status: Passou ✅

## 🧪 CT-01 — Obter mistérios do dia atual

### Endpoint: `GET /day-mysteries`

### Pré-condição:

- API disponível

### Passos:

- Realizar requisição `GET` para `/day-mysteries`

### Resultado esperado:

- Status code 200

- Retorno do tipo de mistério do dia atual

- Payload JSON válido

### Resultado obtido:

- Status code 200

- Tipo do mistério retornado está correto

- Payload retornado conforme esperado

### Status: Passou ✅

## 🧪 CT-02 — Validar estrutura do payload em `/day-mysteries`

### Endpoint: `GET /day-mysteries`

### Pré-condição:

- API disponível

### Passos

- Realizar requisição `GET` para `/day-mysteries`

### Resultado esperado:

- Payload contém:
  - Tipo do mistério

  - Lista de mistérios

  - Campos não nulos

### Resultado obtido:

- Status code 200

- Payload retornado conforme esperado

### Status: Passou ✅

## 🧪 CT-03 — Validar idioma retornado em `/day-mysteries`

### Endpoint: `GET /day-mysteries`

### Pré-condição:

- API disponível

### Passos

- Realizar requisição `GET` para `/day-mysteries`

### Resultado esperado:

- Textos retornados em latim

- Nenhum texto em outro idioma

### Resultado obtido:

- Status code 200

- Todos os textos retornados estão em latim

### Status: Passou ✅

## 🧪 CT-04 — Obter mistérios para dia válido (string)

### Endpoint: `GET /day-mysteries/{day}`

### Pré-condição:

- API disponível

### Passos

- Realizar GET `/day-mysteries/tuesday`

### Resultado esperado:

- Status code 200

- Retorno de mistérios correspondentes à terça-feira

### Resultado obtido:

- Status code 200
- Mistérios corretos para terça-feira retornados

### Status: Passou ✅

## 🧪 CT-05 — Obter mistérios para dia válido (numérico)

### Endpoint: `GET /day-mysteries/{day}`

### Pré-condição:

- API disponível

### Passos

- Realizar `GET /day-mysteries/1`

### Resultado esperado:

- Status code 200

- Retorno de mistérios do domingo

### Resultado obtido:

- Status code 200
- Mistérios do domingo retornados corretamente

### Status: Passou ✅

## 🧪 CT-06 — Validar regra de negócio para segunda-feira

### Endpoint: `GET /day-mysteries/monday`

### Pré-condição:

- API disponível

### Passos

- Realizar `GET /day-mysteries/monday`

### Resultado esperado:

- Tipo dos mistérios retornados: mysteriaGaudiosa

### Resultado obtido:

- Status code 200
- Tipo dos mistérios retornados correto.

### Status: Passou ✅

## 🧪 CT-07 — Validar parâmetro `{day}` case-insensitive

### Endpoint: `GET /day-mysteries/{day}`

### Pré-condição:

- API disponível

### Passos

- Realizar `GET /day-mysteries/MONDAY`

### Resultado esperado:

- Status code 200

- API deve aceitar parâmetro `{day}` de forma case-insensitive

- API deve normalizar o valor do parâmetro `{day}`

- Retorno correto dos mistérios da segunda-feira

### Resultado obtido:

- Status code 400
- Payload atípico no seguinte formato:
  - `{"message" : {}}`

### Status: Falhou ⛔

## 🧪 CT-08 — Validar dia inválido (string)

### Endpoint: `GET /day-mysteries/{day}`

### Pré-condição:

- API disponível

### Passos

- Realizar `GET /day-mysteries/invalidday`

### Resultado esperado:

- Status code 400 ou 404

- Mensagem de erro clara no payload

### Resultado obtido:

- Status code 400
- Payload vago e sem mensagem clara sobre o erro ocorrido, no seguinte formato:
  - `{"message" : {}}`

### Status: Falhou ⛔

## 🧪 CT-09 — Validar dia inválido (numérico fora do intervalo)

### Endpoint: `GET /day-mysteries/{day}`

### Pré-condição:

- API disponível

### Passos

- Realizar `GET /day-mysteries/8`

### Resultado esperado:

- Status code 400 ou 404

- Retorno de erro informando dia inválido

### Resultado obtido:

- Status code 400
- Payload vago e sem mensagem clara sobre o erro ocorrido, no seguinte formato:
  - `{"message" : {}}`

### Status: Falhou ⛔

## 🧪 CT-10 — Validar consistência do payload entre dias diferentes

### Endpoint: `GET /day-mysteries/{day}`

### Pré-condição:

- API disponível

### Passos

- Realizar `GET /day-mysteries/monday`

- Realizar `GET /day-mysteries/tuesday`

### Resultado esperado:

- Estrutura do payload é a mesma

- Apenas os valores mudam

### Resultado obtido:

- Status code 200
- Estrutura do payload não muda
- Valores mudam corretamente conforme o dia

### Status: Passou ✅
