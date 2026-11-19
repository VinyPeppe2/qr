# Leitor QR - Peppe (v3.0)

Aplicação web estática em HTML, CSS e JavaScript.

## Funcionalidades
- Leitura de QR Code e diversos códigos de barras pela câmera ou imagem.
- Tentativa de melhoria de contraste da imagem enviada.
- Copiar, compartilhar, pesquisar e abrir links HTTP/HTTPS.
- Consulta opcional de EAN/UPC na base Open Food Facts (requer internet; cobertura depende da base).
- Gerador de QR Code com tamanho, nível de correção, cores e logotipo opcional.
- Download PNG e cópia de imagem (quando suportado pelo navegador).
- Montagem de QR Pix estático e exibição básica de dados de payload Pix.
- Histórico local de até 100 leituras e exportação CSV.
- Painel de estatísticas, tema claro/escuro e interface PT-BR/EN/ES.
- Estrutura PWA para instalação e cache do shell do app.

## Publicar no GitHub Pages
1. Crie um repositório no GitHub.
2. Extraia o ZIP e envie TODOS os arquivos desta pasta para a raiz do repositório.
3. Abra Settings → Pages.
4. Em Build and deployment, selecione Deploy from a branch, branch `main`, pasta `/ (root)`.
5. Salve. O GitHub Pages publicará o site em HTTPS.

## Importante
- A câmera e a instalação PWA exigem HTTPS ou localhost.
- As bibliotecas html5-qrcode e qrcodejs são carregadas por CDN. A primeira carga exige internet.
- A consulta de produtos usa a API pública Open Food Facts. Nem todo código está cadastrado.
- O gerador Pix monta payload Pix estático e CRC16; não consulta banco, não valida titularidade/chave e não processa pagamentos. Sempre teste no app bancário e confira recebedor e valor.
- O processamento e histórico são locais no navegador, exceto consulta voluntária à base Open Food Facts.
- QR com cores pouco contrastantes ou logotipo grande pode ficar ilegível. Teste antes de imprimir ou distribuir.
