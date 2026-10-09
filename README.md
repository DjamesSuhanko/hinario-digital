# CantusCaeli · páginas públicas Clave Sol

Site independente do aplicativo, com identidade visual Clave Sol. Domínio: **cantuscaeli.clavesol.com.br**.

## Conteúdo

- `content/index.html`: apresentação provisória, sem indexação até receber o conteúdo definitivo.
- `content/privacy.html`: conteúdo integral da política fornecida pelo proprietário, de 9 de outubro de 2026, extraído do HTML entregue. Editar este arquivo para atualizar a política publicada.
- `templates/base.html` e `assets/style.css`: identidade visual compartilhada com MyLuthier/Musicool.
- `assets/cantuscaeli-logo.png`: ícone existente do aplicativo, sem alteração.
- `/privacidade/` e `/privacy.html`: política de privacidade com o mesmo conteúdo.
- `/contato/`: contato do desenvolvedor.

Origem da política: `/home/djames/Documents/Codex/2026-10-08/qu/outputs/CantusCaeli-politica-de-privacidade.html`. O código do CantusCaeli não foi modificado ou incluído.

## Validar localmente

```bash
python3 build.py
python3 scripts/check_site.py
python3 -m http.server 8080 --directory dist
```

## Publicar

GitHub Pages configurado para **GitHub Actions**, com domínio personalizado **cantuscaeli.clavesol.com.br**.

1. No DNS, crie CNAME `cantuscaeli` apontando para `djamessuhanko.github.io` (inicialmente sem proxy).
2. No GitHub, abra **Actions → Publicar CantusCaeli → Run workflow**, selecione `main` e execute.
3. Em **Settings → Pages**, habilite **Enforce HTTPS** quando o certificado estiver disponível.

O commit inicial tem `[skip ci]` para não iniciar o deploy. Os próximos pushes em `main` publicam automaticamente. Somente `dist/` é enviado ao Pages.

Política para o Play Console após o deploy: https://cantuscaeli.clavesol.com.br/privacidade/

A página inicial usa `noindex,follow` enquanto provisória; a política e o contato ficam indexáveis. As fontes são carregadas do Google Fonts, como no site do MyLuthier.
