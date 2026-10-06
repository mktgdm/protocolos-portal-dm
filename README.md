# Protocolos · Portal DM

Biblioteca de protocolos de aplicação dos equipamentos distribuídos pela Dermomed, publicada pelo **GitHub Pages**. Os leads do formulário "Receber os protocolos" vão direto para o **formulário 3 do ActiveCampaign** (dermomed.activehosted.com).

## Arquivos

```
index.html   página completa (HTML, CSS e JS num arquivo só)
.nojekyll    faz o GitHub Pages servir os arquivos sem processar
README.md    este guia
```

## Publicar

1. Crie um repositório **público** no GitHub (o Pages gratuito exige repositório público) e envie estes arquivos para a raiz.
2. No repositório: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root) → Save**.
3. Em 1–2 minutos o site fica em `https://<usuario>.github.io/<repositorio>/`.

## Leads e entrega dos protocolos

- O formulário envia nome, e-mail, telefone (+55) e perfil (`field[7]`) para o formulário 3 do ActiveCampaign.
- A entrega do material é feita por uma **automação no ActiveCampaign**: gatilho "Envia o formulário 3" → e-mail com o link dos protocolos.
- Os IDs ficam no objeto `CONFIG.activecampaign`, no começo do `<script>` do `index.html`.

## Editar protocolos

No GitHub Pages não há servidor, então a área restrita da equipe fica desativada. Para alterar protocolos, edite a lista `SEMENTE` no `index.html` (lápis de edição no GitHub) — cada commit publica o site de novo.
