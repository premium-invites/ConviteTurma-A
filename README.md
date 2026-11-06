# Formatura do ABC — CEPA | Turmas A e B

Este pacote foi recriado com base no projeto de referência `Mari-Bezerra-main (1).zip`.

## Estrutura

- A Turma A fica na raiz do repositório (`index.html`, `config.js`, `assets/`).
- A Turma B fica na pasta `turma-b/`.
- Os arquivos compartilhados (abertura, música e manual) ficam em `assets/` na raiz.
- Cada turma tem seu próprio vídeo principal, poster e capa do WhatsApp.

## Requisitos atendidos

- Não existe arquivo `.css` separado: as regras visuais ficam dentro do `<style>` do `index.html`, seguindo o ZIP de referência.
- Não existe arquivo `app.js`/`script.js` separado: a engine fica embutida no HTML.
- `config.js` é pequeno e contém somente as configurações do convite e as posições dos hotspots.
- A página abre diretamente no vídeo `opening.mp4`, sem tela intermediária “Toque para abrir”.
- O vídeo de abertura tenta iniciar automaticamente com áudio. Se o navegador bloquear áudio automático, ele tenta iniciar silenciosamente e exibe apenas o controle discreto “Ativar som”.
- O botão “Pular vídeo” encerra a abertura e leva ao vídeo principal.
- Ao terminar ou pular a abertura, o vídeo principal da turma começa em loop e a música MP3 começa a tocar.
- O vídeo principal não tem botões gráficos sobrepostos. As áreas de clique de Localização e Manual são transparentes e coincidem com os botões já desenhados no próprio vídeo.
- O botão Manual abre a imagem `manual.webp` em tela cheia. O botão “Voltar” retorna ao vídeo principal.
- O editor de áreas continua disponível em `?editor=1`.

## Mídias e caminhos

### Turma A (raiz)
- `assets/opening.mp4`: abertura com a história do livro.
- `assets/video.mp4`: vídeo principal da Turma A.
- `assets/musica.mp3`: trilha que começa depois da abertura.
- `assets/manual.webp`: arte do Manual do Convidado.
- `assets/preview-whatsapp.jpg`: capa 1200 × 630 da Turma A.

### Turma B (`turma-b/`)
- `turma-b/assets/video.mp4`: vídeo principal da Turma B.
- `turma-b/assets/preview-whatsapp.jpg`: capa 1200 × 630 da Turma B.
- Os arquivos de abertura, música e manual são compartilhados com a raiz.

## Publicação no GitHub Pages

1. Extraia este ZIP.
2. Abra a pasta `CEPA_REFEITO_V4`.
3. Envie **o conteúdo de dentro dela** para a raiz do repositório GitHub (não envie a pasta externa inteira como um nível adicional).
4. Confira se o repositório ficou com `index.html`, `config.js`, `assets/` e `turma-b/` na raiz.
5. Apague os arquivos antigos `styles.css`, `app.js`, `manual.html` e qualquer outro `.css`/`app.js` externo da versão anterior. A nova engine não usa esses arquivos separados.
6. No GitHub, abra **Settings → Pages**.
7. Em **Build and deployment**, selecione **Deploy from a branch**.
8. Selecione a branch `main` e a pasta `/ (root)`, depois salve.

### Links resultantes

- Turma A: `https://SEU-USUARIO.github.io/SEU-REPOSITORIO/`
- Turma B: `https://SEU-USUARIO.github.io/SEU-REPOSITORIO/turma-b/`

### Prévia do WhatsApp

O HTML já contém os metadados Open Graph para cada turma, mas o endereço está com o marcador `SEU-USUARIO/SEU-REPOSITORIO`.

Depois de publicar, substitua esse marcador:
- no `index.html` da raiz, pelo endereço real da Turma A;
- no `turma-b/index.html`, pelo endereço real da Turma B.

As capas `assets/preview-whatsapp.jpg` já estão em 1200 × 630 pixels. O WhatsApp pode manter a prévia em cache por algum tempo.

## Editor de áreas invisíveis

Abra:
- Turma A: `https://SEU-USUARIO.github.io/SEU-REPOSITORIO/?editor=1`
- Turma B: `https://SEU-USUARIO.github.io/SEU-REPOSITORIO/turma-b/?editor=1`

No editor:
1. Selecione Localização ou Manual do Convidado.
2. Arraste a área transparente até coincidir com o botão desenhado no vídeo.
3. Arraste a alça do canto para redimensionar.
4. Clique em **Copiar código**.
5. Cole o bloco gerado dentro de `hotspots` no `config.js` da turma correspondente.
6. Para ajustar o botão de voltar do Manual, selecione “Voltar — Manual do Convidado” e ajuste-o também.

O editor salva uma cópia local no navegador e gera o código para você colar no `config.js`; ele não grava diretamente no GitHub.

## Dados do evento configurados

- Formatura do ABC — CEPA
- Data: 05/12/2026
- Horário: 18h30
- Local: Mistura Fina Buffet
- Localização: link do Google Maps fornecido na conversa.

## Observação importante sobre o Manual

A arte atual do Manual contém sugestões de chegada antecipada, traje social/esporte fino, fotografias e celular no silencioso. Essas orientações foram propostas como exemplo e ainda precisam ser confirmadas pela organização antes de divulgar o convite publicamente.
