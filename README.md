# YourSite — landing page

Site estático, sem etapa de build e sem dependências de npm. Pronto para GitHub + Vercel.

## Estrutura
- `index.html` — página (template + lógica).
- `support.js` — runtime que renderiza a página (usa o React 18.3.1 local de `vendor/`, sem CDN).
- `image-slot.js` — componente das imagens do carrossel da hero.
- `vendor/` — React e ReactDOM 18.3.1.
- `assets/` — imagens (WebP), vídeos, logos, páginas completas dos projetos (`assets/full/`), favicon e imagem de compartilhamento.
- `vercel.json` — cache dos arquivos estáticos e cabeçalhos de segurança.
- `robots.txt`, `favicon.ico`, `.gitignore`.

## Deploy na Vercel
1. Envie o conteúdo desta pasta para um repositório no GitHub (os arquivos na raiz do repositório).
2. Vercel → Add New → Project → Import do repositório.
3. Framework Preset: **Other**. Build Command: vazio. Output Directory: vazio (raiz). Install Command: vazio.
4. Deploy.

## Variáveis de ambiente
Nenhuma. O site não usa chaves, APIs privadas ou credenciais.

## Testar localmente
    python3 -m http.server 8080
Abra http://localhost:8080 (precisa ser servido por HTTP; abrir o arquivo direto não funciona).

## Pendências externas
- Domínio de produção: quando definido, adicionar `<link rel="canonical">`, `og:url` e trocar `og:image`/`twitter:image` para URL absoluta (ex.: `https://SEU-DOMINIO/assets/og-image.png`) no `<head>` do `index.html`.
- E-mail de contato: `contatoyoursite@gmail.com` (os botões de e-mail abrem o Gmail em nova aba; para usar o app de e-mail do visitante, troque em `index.html` a linha `mailto:` no `renderVals`).
- Testar em Safari (iPhone/Mac) e Firefox após publicar.
