# 🧠 CodelabS Checker – API REST em Node.js

**Área:** Backend – Desenvolvimento de API  
**Tecnologias:** Node.js + Express.js

## ✨ Sobre o projeto

Este projeto foi desenvolvido como parte do desafio de férias do [USP CodeLab](https://codelab.dev.br), com o objetivo de criar uma API REST que ajude a combater os inúmeros erros na escrita do nome do nosso grupo.

Muitas pessoas ainda insistem em variações como:

- `Codelabs`
- `Code labe`
- `Codalab`
- `Codeslab`
- `Codeleb`
- e outras variações absurdas…

Nossa missão? Monitorar, registrar e organizar esses erros — transformando frustração em dados úteis!

---

## 🔧 Como funciona

A API centraliza a coleta dos nomes digitados e armazena dois grupos:

- ✅ Nomes corretos (`"codelab", e quaisquer outras variações maiúsculas ou minúsculas`)
- ❌ Nomes incorretos (qualquer outro)

Esses dados são salvos em um arquivo `nomes.json`, e podem ser analisados depois.

---

## 🚀 Como rodar o projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/BrunoZuffo/projeto-codelab.git
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Inicie o servidor com:
   ```bash
   npm run dev
   ```

O servidor estará disponível em:  
📍 `http://localhost:3000`

---

## 📮 Endpoints disponíveis

### `GET /`

- Retorna uma mensagem de boas-vindas da API.

---

### `POST /nome`

- Envie um corpo JSON com um nome:

```json
{
  "nome": "codelab"
}
```

- A API irá:

  - Verificar se o nome é igual a `"codelab"`
  - Registrar como **correto** ou **incorreto** no arquivo `nomes.json`
  - Retornar uma mensagem indicando o resultado

---

## 📁 Estrutura do banco de dados (`nomes.json`)

```json
{
  "corretos": [
    {
      "nome": "codelab",
      "data": "2025-08-01T03:15:22.711Z"
    }
  ],
  "incorretos": [
    {
      "nome": "codelabs",
      "data": "2025-08-01T03:17:08.152Z"
    }
  ]
}
```

---

## 🤓 Autor

Projeto feito com 💜 por Bruno Zuffo durante o recesso, como parte da missão de proteger a identidade do grupo CodeLab.
