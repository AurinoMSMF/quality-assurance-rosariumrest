### 🐞 BUG-02 — Payload de erro genérico para dia inválido (string)

- #### ID: BUG-02
- #### Relacionado ao CT: CT-08
- #### Endpoint: `GET /day-mysteries/{day}`
- #### Ambiente: Produção (Vercel)
- #### Severidade: Baixa
- #### Prioridade: Média
- #### Status: Aberto

### 📝 Descrição

- Quando um valor inválido em formato string é enviado no parâmetro `{day}`, a API retorna erro 400 com payload genérico, sem mensagem clara informando a causa do erro.

### 🔁 Passos para reproduzir

- Realizar requisição `GET /day-mysteries/invalidday`

### ✅ Resultado esperado

- Status code 400 ou 404

- Payload com mensagem clara indicando que o dia informado é inválido

### ❌ Resultado obtido

- Status code 400

- Payload retornado no formato:
  - `{ "message": {} }`

### 📌 Observações

- Mensagens de erro mais descritivas facilitam o consumo da API e o diagnóstico de problemas por parte do cliente.
