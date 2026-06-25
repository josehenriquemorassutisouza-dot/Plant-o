# PLANTÃO — app de apoio à decisão (PWA)

App web mobile-first para consulta rápida no plantão (UPA/PS). Navegação por sistema,
busca por doença, e **botão Copiar** em cada bloco para colar no prontuário.
Funciona offline e pode ser **instalado** na tela inicial do celular.

> **Aviso:** material de apoio à decisão, para uso por profissional habilitado.
> Não substitui o julgamento clínico. Confira as doses caso a caso.

## Conteúdo
- 13 categorias · 64 fichas (faixa Adulto). Pediátrico/Gestante: em construção.

## Como hospedar grátis no GitHub Pages
1. Crie um repositório novo (ex.: `plantao`) no GitHub.
2. Envie **todos os arquivos desta pasta** para o repositório
   (`index.html`, `manifest.json`, `sw.js`, `icon-*.png`, `apple-touch-icon.png`).
3. No repositório: **Settings → Pages** → em *Branch* escolha `main` e pasta `/ (root)` → **Save**.
4. Aguarde ~1 min. O endereço será algo como `https://SEU-USUARIO.github.io/plantao/`.
5. Abra no celular e use **"Adicionar à tela de início"** (Android: menu do Chrome / iPhone: Compartilhar → Adicionar à Tela de Início).

> Como é um PWA, depois de aberto uma vez ele funciona **sem internet**.
> O cache do service worker é versionado automaticamente (hash do conteúdo) a cada build; o app atualiza sozinho quando online.

## Para testar localmente no computador
Na pasta do app, rode: `python3 -m http.server 8080` e abra `http://localhost:8080`.
(O app precisa ser servido por http/https para o modo offline/instalação funcionarem — abrir o arquivo direto também mostra o conteúdo, mas sem PWA.)

## Como editar o conteúdo
As fichas foram geradas a partir dos arquivos `Plantao_Fase*.md`. Para mudanças pontuais de texto,
é possível editar direto no `index.html` (bloco `app-data`). Para mudanças maiores, edite os `.md`
e gere o app novamente.
