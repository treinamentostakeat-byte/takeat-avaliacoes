# Takeat — Plataforma de Avaliações

Sistema de avaliação de atendimento dos colaboradores Takeat pelos restaurantes clientes.

## Arquivos

| Arquivo | Descrição |
|---------|-----------|
| `index.html` | Página inicial com links para as duas áreas |
| `takeat-avaliacao-cliente.html` | Formulário para o restaurante avaliar |
| `takeat-avaliacoes.html` | Painel do gestor com dashboard e relatórios |

## Como hospedar no GitHub Pages (gratuito)

### Passo 1 — Criar conta no GitHub
1. Acesse **github.com** e crie uma conta gratuita (se não tiver)

### Passo 2 — Criar repositório
1. Clique em **"New repository"** (botão verde)
2. Nome do repositório: `takeat-avaliacoes`
3. Marque como **Public**
4. Clique em **"Create repository"**

### Passo 3 — Fazer upload dos arquivos
1. Na página do repositório, clique em **"uploading an existing file"**
2. Arraste os 4 arquivos:
   - `index.html`
   - `takeat-avaliacao-cliente.html`
   - `takeat-avaliacoes.html`
   - `README.md`
3. Clique em **"Commit changes"**

### Passo 4 — Ativar GitHub Pages
1. Vá em **Settings** (engrenagem)
2. No menu esquerdo, clique em **Pages**
3. Em "Source", selecione **Deploy from a branch**
4. Branch: **main** → pasta: **/ (root)**
5. Clique em **Save**

### Passo 5 — Acessar os links
Após 1-2 minutos, seus links estarão disponíveis:

- **Hub principal:** `https://SEU_USUARIO.github.io/takeat-avaliacoes/`
- **Clientes (restaurantes):** `https://SEU_USUARIO.github.io/takeat-avaliacoes/takeat-avaliacao-cliente.html`
- **Painel do gestor:** `https://SEU_USUARIO.github.io/takeat-avaliacoes/takeat-avaliacoes.html`

## Firebase — Regras de segurança

Acesse o Firebase Console → Firestore Database → Regras e publique:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /avaliacoes/{doc} {
      allow write: if true;
      allow read: if true;
    }
  }
}
```

## Suporte
Plataforma desenvolvida para uso interno da Takeat.
