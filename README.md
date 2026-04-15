# Survey123 → Ficha de Cadastro

Página web que roda 100% no navegador e no GitHub Pages.
Sem servidor, sem créditos ArcGIS, sem GitHub Actions.

## Como funciona

1. Você abre a página no navegador
2. Digita usuário, senha e URL do Feature Layer
3. A tabela de cadastros aparece — busca em qualquer campo
4. Clica "Baixar" → o `.docx` é gerado e baixado na hora

Tudo roda no seu navegador. As credenciais são usadas só para
obter um token temporário direto na API do ArcGIS.

## Publicar no GitHub Pages (fazer uma vez)

1. Crie um repositório **privado** no GitHub
2. Faça upload de todos os arquivos deste ZIP
3. Vá em **Settings → Pages**
4. Source: **GitHub Actions**
5. Dê um push ou clique em **Actions → Deploy GitHub Pages → Run workflow**
6. A URL da sua página aparece em Settings → Pages

## Estrutura

```
docs/
  index.html               ← Página web completa
  FICHA_DE_CADASTRO.docx   ← Modelo Word (não altere o nome)
.github/workflows/
  deploy.yml               ← Publica docs/ no GitHub Pages
```

## Nota sobre repositório privado

O GitHub Pages de repositórios privados exige plano pago.
Alternativa gratuita: use **Netlify** (arraste a pasta `docs/` em netlify.com/drop)
ou abra o `index.html` diretamente no navegador — funciona sem servidor.
