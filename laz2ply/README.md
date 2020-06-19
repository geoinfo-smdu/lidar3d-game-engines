# Convertendo um arquivoo LAZ para PLY

Muitas game engines acabam não lendo o formato LAZ que originalmente é disponibilizado quando o download é realizado pelo site do (GeoSampa)[http://geosampa.prefeitura.sp.gov.br/PaginasPublicas/_SBC.aspx], para isso vamos monstrar como converter a partir de um arquivos LAZ.

Como exemplo vamos baixar uam região definida pelo SCM 3314-133 que pode ser visualizada pelo link https://visualizador-laz-web.s3-sa-east-1.amazonaws.com/index.html?scm=3314-133

E para isso vamos baixar o arquivo https://laz-m3dc-pmsp.s3-sa-east-1.amazonaws.com/MDS_color_3314-133.laz e copia-lo para a pasta `data` ou redefinir um local a partir do arquivo `laz2ply.json`

## Utiliando a bilbioteca PDAL

Quem vai fazer o trabalho de conversão é a biblioteca (Pdal)[https://pdal.io/] no site vc deve encontrar informações de como instala-la. Apesar de ser uma biblioteca para manipulação de nuvem de pontos em Python possui uma linha de comando que vamos utilizar aqui

DEpois de devidamente instalada vamos chamar o `pdal` indicando que o `pipeline` que queremos executar está no arquivo `laz2ply.json` dessa forma:

`pdal pipeline ept2ply/ept2ply.json`

Se tudo deu certo, um novo arquivo vai estar na pasta `results`. Não vamos disponibilizar o resultado aqui pois o arquivo é demasiadamente grande para o GitHub, mas vamos publicar em um link temporário https://we.tl/t-0fGS575lpD
