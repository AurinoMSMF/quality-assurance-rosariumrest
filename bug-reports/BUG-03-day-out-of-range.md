## 🐞 BUG-03 — Payload de erro genérico para dia inválido (numérico fora do intervalo)

- #### ID: BUG-03
- #### Relacionado ao CT: CT-09
- #### Endpoint: `GET /day-mysteries/{day}`
- #### Ambiente: Produção (Vercel)
- #### Severidade: Baixa
- #### Prioridade: Média
- #### Status: Aberto

### 📝 Descrição

- Ao informar um valor numérico fora do intervalo esperado (1 a 7) no parâmetro `{day}`, a API retorna erro 400 com payload genérico, sem detalhamento da causa.

### 🔁 Passos para reproduzir

- Realizar requisição `GET /day-mysteries/8`

### ✅ Resultado esperado

- Status code 400 ou 404

- Mensagem de erro indicando que o valor numérico está fora do intervalo permitido

### ❌ Resultado obtido

- Status code 400

- Payload retornado no formato:
  - `{ "message": {} }`

### 📌 Observações

- A validação já existe, porém o payload de erro não informa adequadamente o motivo da falha.
