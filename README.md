# Protocolos · Portal DM

Biblioteca de protocolos de aplicação dos equipamentos distribuídos pela Dermomed, publicada pelo **GitHub Pages**.

## Arquivos

```
index.html        página completa (HTML, CSS e JS num arquivo só)
protocolos.json   catálogo de seções e protocolos — é ele que a área restrita edita
.nojekyll         faz o GitHub Pages servir os arquivos sem processar
README.md         este guia
```

## Publicar

1. Crie um repositório **público** no GitHub e envie estes arquivos para a raiz.
2. **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
3. Em 1–2 minutos o site fica em `https://<usuario>.github.io/<repositorio>/`.

## Editar os protocolos (área restrita)

No rodapé da página, **Área restrita da equipe** abre o painel. Quem edita entra com um **token do GitHub**:

1. GitHub → foto → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. *Repository access*: **Only select repositories** → este repositório.
3. *Permissions → Repository permissions → Contents*: **Read and write**.
4. Gere e guarde o token (`github_pat_…`) — ele aparece uma vez só.

Ao clicar em **Publicar**, o painel grava o `protocolos.json` direto no repositório (um commit por publicação). O GitHub Pages atualiza o site em 1–2 minutos. Para desfazer uma publicação, abra o histórico do `protocolos.json` no GitHub e reverta o commit.

O repositório é detectado pelo endereço `usuario.github.io/repositorio`. Se usar domínio próprio, preencha `CONFIG.github` (dono e repo) no começo do `<script>` do `index.html`.

As artes continuam no **Google Drive**: no editor de cada protocolo, cole o link do arquivo. A pasta precisa estar compartilhada como "qualquer pessoa com o link".

## Leads

O formulário "Receber os protocolos" envia nome, e-mail, telefone (+55) e perfil (`field[7]`) para o **formulário 3 do ActiveCampaign** (dermomed.activehosted.com). A entrega do material é feita por uma automação no ActiveCampaign com gatilho "Envia o formulário 3". Os IDs ficam em `CONFIG.activecampaign`.
