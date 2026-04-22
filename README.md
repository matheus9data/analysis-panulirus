# Análise Espacial e Distribuição de Panulirus spp.

Este projeto contém um pipeline de dados em R estruturado para limitar, processar e mapear a distribuição geográfica das espécies *Panulirus spp.*. 

O objetivo principal deste script é transformar dados brutos de corrosão (com potenciais erros de formação e coordenadas inconsistentes) em **visualizações espaciais precisas** para tomada de decisão em conservação.

### Tecnologias e Pacotes Utilizados
* **Linguagem:** R
* **Manipulação de Dados:** `dplyr`, `tidyr`
* **Processamento Geoespacial:** `sf` (Características simples), `terra`
* **Visualização de dados:** `ggplot2`

### Arquitetura 

1. **Ingestão e Limpeza (`data_cleaning.R`):** 
   - Tratamento de valores nulos (NAs) nas coordenadas geográficas.
   - Padronização de strings nos nomes de localização.
   - Exportação do conjunto de dados limpo para `/dados/processado/`.
2. **Modelagem e Mapeamento (`mapeamento_espacial.R`):**
   - Conversão do dataframe em objetos espaciais (sf).
   - Cruzamento com *arquivos de forma* do contorno costeiro.
   - Geração de mapas de calor/distribuição exportados para `/saídas/`.

### Resultados (Amostra)
![Mapa de Ocorrência](saídas/mapa_distribuicao.png)

### Como executar este projeto
Clone este repositório e certificado-se de que o seu *diretoria de trabalho* é a raiz do projeto. Ó pacote `aqui` gerenciará os caminhos automaticamente.
```batedor
clone git [https://github.com/matheus9dados/nome-do-repositorio.git](https://github.com/matheus9dados/nome-do-repositorio.git)
