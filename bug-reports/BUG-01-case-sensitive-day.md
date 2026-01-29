### 🐞 BUG-01 — Parâmetro {day} não aceita valor em uppercase

- #### ID: BUG-01
- #### Relacionado ao CT: CT-07
- #### Endpoint: `GET /day-mysteries/{day}`
- #### Ambiente: Produção (Vercel)
- #### Severidade: Média
- #### Prioridade: Média
- #### Status: Aberto

### 📝 Descrição

- A API não aceita valores em uppercase no parâmetro `{day}`, retornando erro 400 ao invés de processar corretamente o dia informado.

### 🔁 Passos para reproduzir

- Realizar requisição GET `/day-mysteries/MONDAY`

### ✅ Resultado esperado

- Status code 200

- Retorno correto dos mistérios correspondentes à segunda-feira

- API deve tratar o parâmetro `{day}` de forma case-insensitive

### ❌ Resultado obtido

- Status code 400

- Payload retornado no formato:
  - `{ "message": {} }`

### 📌 Observações

- A ausência de normalização do parâmetro pode causar falhas desnecessárias em integrações que enviem valores em uppercase.
