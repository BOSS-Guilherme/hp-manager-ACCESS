# hp-manager-ACCESS

<div align="center">

# 🛠️ HP Manager

**Gerenciador de repositórios do GitHub**

Painel web que permite gerenciar outros repositórios: enviar, atualizar e apagar arquivos de forma prática, direto pelo site.

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Vercel](https://img.shields.io/badge/deploy-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![API](https://img.shields.io/badge/API-%2Fapi%2Ffiles-blue?style=for-the-badge)

</div>

---

## 📖 Sobre

O **HP Manager** permite **gerenciar outros repositórios** do GitHub: **enviar**, **atualizar**, **apagar** arquivos e muito mais, tudo por um site protegido por uma chave de administrador.

## ✨ Funcionalidades

- 📤 Enviar arquivos para um repositório
- 🔄 Atualizar arquivos existentes
- 🗑️ Apagar arquivos
- 📋 Listar os arquivos do repositório (Refresh list)
- 🔑 Acesso protegido por `ADMIN_KEY`

## ⚙️ Como usar localmente

1. Copie `.env.example` para `.env` e preencha os valores (token do GitHub, usuário, repositório e uma `ADMIN_KEY`).
2. Instale as dependências:

```
npm install
```

3. Abra o servidor e o site juntos:

```
npm run dev
```

4. No site, digite a `ADMIN_KEY` e clique em **Refresh list**.

## 🚀 Deploy na Vercel

1. Suba o projeto para um repositório no GitHub (o `.env` não vai, ele está no `.gitignore`).
2. Na Vercel: **Add New > Project** e importe o repositório. O `vercel.json` já define o build (`npm run build`) e a saída (`dist`).
3. Em **Settings > Environment Variables**, cadastre as variáveis abaixo.
4. Faça o deploy. A API roda em `/api/files` (arquivo `api/files.mjs`), no mesmo domínio do site.

### 🔐 Variáveis de ambiente

| Variável | Descrição |
|----------|-----------|
| `GITHUB_TOKEN` | Token de acesso do GitHub |
| `GITHUB_OWNER` | Usuário dono do repositório |
| `GITHUB_REPO` | Repositório que será gerenciado |
| `GITHUB_BRANCH` | Branch usada |
| `GITHUB_FOLDER` | Pasta onde ficam os arquivos |
| `ADMIN_KEY` | Chave de administrador para acessar o site |

## ⚠️ Limite de upload

A Vercel aceita requisições de até **~4,5 MB**, então arquivos acima de **~3 MB** não sobem.

---

<div align="center">

Feito por [Guilherme](https://github.com/BOSS-Guilherme)

</div>
