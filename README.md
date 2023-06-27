
# InstaColors

Este repositório contém um script Python chamado `InstaColors.py` que utiliza dos dados coletados atraves do CrowdTangle para baixar imagens do Instagram, coletar a cor predominante de cada imagem, extrair dados como numero de likes, interações, comentarios e gerar uma visualização interativa em HTML com as cores encontradas.

## Processo de Desenvolvimento

 - [x] Download das imagens a partir do CSV fornecido pelo CrowdTangle
 - [x] Extração dos dados de Likes, Interações, Comentários do CSV
 - [x] Analise da cor predominante de cada imagem
 - [x] Implementação das organizações dos itens por Saturação, Brilho, Matiz, Nº Likes, Nº Comentarios, Nº Interações 
 - [ ] Implementação da pre-visualização das imagens
 - [ ] Tamanho do .colordot adaptável ao numero de itens no dataset
 - [ ] Restruturação da estética da página 

## Requisitos

Certifique-se de ter instalado as seguintes dependências antes de executar o script:

-   Python 3.6 ou superior.
-   Bibliotecas Python: `requests`, `pandas`, `tqdm`, `colorthief`, `urllib`, `PIL`, `bs4`.



## Uso

1.  Clone este repositório para o seu ambiente local.
2.  Certifique-se de ter todas as dependências instaladas.
3.  Execute o script `InstaColors.py` utilizando o Python 3.
4.  As imagens serão baixadas para o diretório `imagensinsta`.
5.  As cores predominantes de cada imagem serão coletadas e salvas em um arquivo CSV chamado `dados_cores_insta.csv`.
6.  Será gerados 6 arquivos HTML  que representam as organizações das visualização a partir das cores e dados coletados.

## Funcionalidades

-   Baixar imagens do Instagram: o script baixa imagens a partir de URLs fornecidas em um arquivo CSV.
-   Coletar cores predominantes: o script utiliza a biblioteca `colorthief` para identificar a cor predominante de cada imagem.
-   Gerar visualização em HTML: o script gera um arquivo HTML que apresenta uma visualização das cores encontradas, incluindo informações como número de curtidas e comentários relacionados a cada imagem.

## Personalização

Você pode personalizar o script de acordo com suas necessidades. Algumas opções de personalização incluem:

-   Alterar o diretório de destino para salvar as imagens, modificando a variável `destination_directory`.
-   Modificar as extensões de arquivo suportadas para baixar apenas determinados tipos de imagens, alterando a lista `image_extensions`.
-   Personalizar a ordem das cores na visualização em HTML, alterando a lista `ordem_cores` no método `generate_html_visualization`.

## Limitações

-   O script depende da disponibilidade de URLs das imagens no arquivo CSV fornecido.
-   A detecção da cor predominante pode não ser precisa em todas as imagens, dependendo da qualidade da imagem e da diversidade das cores presentes.

## Observações

Este script foi desenvolvido com base nas informações disponíveis até Junho de 2023 e pode não ser compatível com todas as versões futuras do Instagram ou CrowdTangle.
