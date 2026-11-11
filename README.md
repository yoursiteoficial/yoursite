# YourSite — landing page

Site estático, sem etapa de build e sem dependências de npm. Pronto para GitHub + Vercel.

## Estrutura
- `index.html` — página (template + lógica).
- `support.js` — runtime que renderiza a página (usa o React 18.3.1 local de `vendor/`, sem CDN).
- `image-slot.js` — componente das imagens do carrossel da hero.
- `vendor/` — React e ReactDOM 18.3.1.
- `assets/hero/` — imagens dos 18 projetos (cards, miniaturas e carrossel da hero).
- `assets/full/` — páginas completas dos 18 projetos (botão "Expandir").
- `assets/comparativo/`, `assets/feedbacks/`, `assets/favicon/`, `assets/og-image.png`, logos.
- `vercel.json` — cache dos arquivos estáticos e cabeçalhos de segurança.
- `robots.txt`, `favicon.ico`, `.gitignore`.

## Meta Pixel
O Pixel da Meta (ID 1660504892391997) e a verificação de domínio do Facebook estão no início do `<head>` do `index.html`,
copiados sem alteração da versão em produção.

## Atualizar o repositório
Substitua todo o conteúdo do repositório pelo conteúdo desta pasta (os arquivos ficam na raiz do repositório).
Apague do repositório arquivos que não existem mais aqui, por exemplo `.image-slots.state.json` e as imagens
`assets/hero/projeto-10/11/12` e `assets/full/projeto-10/11/12` (projetos removidos).
Observação: no Mac, arquivos que começam com ponto (`.gitignore`) ficam ocultos no Finder (Cmd + Shift + . mostra).
O site funciona sem eles.

## Deploy na Vercel
1. Vercel → Add New → Project → Import do repositório.
2. Framework Preset: **Other**. Build Command: vazio. Output Directory: vazio (raiz). Install Command: vazio.
3. Deploy. Nenhuma variável de ambiente.

## Testar localmente
    python3 -m http.server 8080
Abra http://localhost:8080 (precisa ser servido por HTTP; abrir o arquivo direto não funciona).

## Pendências externas
- Domínio de produção: quando definido, adicionar `<link rel="canonical">`, `og:url` e trocar `og:image`/`twitter:image`
  para URL absoluta (ex.: `https://SEU-DOMINIO/assets/og-image.png`) no `<head>` do `index.html`.
- E-mail de contato: `contatoyoursite@gmail.com` (os botões de e-mail abrem o Gmail em nova aba).
- Validar no Safari (Mac, iPad e iPhone) e no Firefox depois de publicar.
