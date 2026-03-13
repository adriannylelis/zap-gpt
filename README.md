
# zap-gpt 🤖

![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?logo=node.js&logoColor=white)
![License](https://img.shields.io/badge/license-ISC-blue)
![OpenAI](https://img.shields.io/badge/OpenAI-API-412991?logo=openai&logoColor=white)
![WhatsApp](https://img.shields.io/badge/WhatsApp-Web.js-25D366?logo=whatsapp&logoColor=white)

Integração entre **WhatsApp** e a **API da OpenAI** que permite gerar respostas de texto com o modelo GPT (Davinci) e imagens com o **DALL-E** diretamente pelo WhatsApp, de forma totalmente automatizada.



---

## ✨ Funcionalidades

- 💬 **Geração de texto** via GPT (modelo `text-davinci-003`) com o comando `/bot`
- 🎨 **Geração de imagens** via DALL-E com o comando `/img`
- 📲 Funciona em conversas individuais e em grupos do WhatsApp
- 🔒 Autenticação persistente com `LocalAuth` (sem necessidade de escanear QR Code a cada reinício)

---

## 🛠️ Tecnologias

| Tecnologia | Descrição |
|---|---|
| [Node.js](https://nodejs.org/) | Ambiente de execução JavaScript |
| [whatsapp-web.js](https://wwebjs.dev/) | Biblioteca para integração com WhatsApp Web |
| [OpenAI API](https://platform.openai.com/docs/) | API para geração de texto (GPT) e imagens (DALL-E) |
| [axios](https://axios-http.com/) | Cliente HTTP para chamadas à API |
| [dotenv](https://github.com/motdotla/dotenv) | Gerenciamento de variáveis de ambiente |
| [qrcode-terminal](https://github.com/gtanner/qrcode-terminal) | Exibição do QR Code no terminal |

---

## ⚙️ Pré-requisitos

- [Node.js](https://nodejs.org/) 18 ou superior
- [npm](https://www.npmjs.com/) 8 ou superior
- Uma conta na [OpenAI](https://platform.openai.com/) com créditos disponíveis
- Um número de WhatsApp ativo para conectar o bot

---

## 🚀 Configuração e execução

### 1. Clone o repositório

```bash
git clone https://github.com/adriannylelis/zap-gpt.git
cd zap-gpt
```

### 2. Configure as variáveis de ambiente

Copie o arquivo de exemplo e preencha com suas credenciais:

```bash
cp .env.example .env
```

Edite o arquivo `.env`:

```env
OPENAI_KEY=sk-sua-chave-aqui
PHONE_NUMBER=5511999999999
```

> Veja a seção [Variáveis de Ambiente](#-variáveis-de-ambiente) para mais detalhes.

### 3. Instale as dependências

```bash
npm install
```

### 4. Inicie o projeto

```bash
npm start
```

Um QR Code será exibido no terminal. Abra o WhatsApp no seu celular, vá em **Configurações → Aparelhos conectados → Conectar um aparelho** e escaneie o código.

> Após a primeira autenticação, as credenciais são salvas localmente e o QR Code não será exibido novamente.

---

## 💬 Comandos disponíveis

| Comando | Descrição | Exemplo |
|---|---|---|
| `/bot <pergunta>` | Gera uma resposta de texto usando o GPT (Davinci) | `/bot Qual a capital da França?` |
| `/img <descrição>` | Gera uma imagem usando o DALL-E | `/img Um gato astronauta no espaço` |

---

## 🔑 Variáveis de Ambiente

| Variável | Descrição | Exemplo |
|---|---|---|
| `OPENAI_KEY` | Chave de API da OpenAI. Obtenha em [platform.openai.com](https://platform.openai.com/api-keys) | `sk-abc123...` |
| `PHONE_NUMBER` | Número de telefone vinculado à conta do WhatsApp (somente dígitos, com DDI e DDD) | `5511999999999` |

---

## 📁 Estrutura do projeto

```
zap-gpt/
├── index.js          # Lógica principal do bot
├── .env.example      # Exemplo de configuração de variáveis de ambiente
├── package.json      # Dependências e scripts do projeto
└── README.md         # Documentação
```

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*.

1. Faça um fork do projeto
2. Crie uma branch para sua feature: `git checkout -b feat/minha-feature`
3. Commit suas alterações: `git commit -m 'feat: minha nova feature'`
4. Faça push para a branch: `git push origin feat/minha-feature`
5. Abra um Pull Request

---

## 📄 Licença

Este projeto está licenciado sob a licença **ISC**. Consulte o arquivo [LICENSE](LICENSE) para mais informações.
[referencia Tab News](https://www.tabnews.com.br/victorharry/guia-completo-de-como-integrar-o-chat-gpt-com-whatsapp)
---

<p align="center">Feito com ❤️ — não esqueça de dar uma ⭐ no repositório!</p>
