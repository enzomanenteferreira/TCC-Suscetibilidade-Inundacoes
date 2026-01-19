# Mapeamento de Áreas de Risco em Foz do Iguaçu – Suscetibilidade a Inundações

Este repositório contém os códigos, dados processados e modelos desenvolvidos no Trabalho de Conclusão de Curso (TCC) do curso de Ciência da Computação da Universidade Estadual do Oeste do Paraná (UNIOESTE), Campus de Foz do Iguaçu.

O trabalho tem como objetivo o desenvolvimento de um modelo de mapeamento de suscetibilidade a inundações no município de Foz do Iguaçu–PR, por meio da integração de técnicas de geoprocessamento, sensoriamento remoto e aprendizado de máquina, com foco no apoio ao planejamento urbano e à gestão de riscos socioambientais.

---

## 📌 Contextualização

O crescimento urbano desordenado aliado à intensificação de eventos climáticos extremos tem aumentado a recorrência de alagamentos urbanos em Foz do Iguaçu, especialmente em regiões de baixa altitude, próximas a cursos d’água e com elevado grau de impermeabilização do solo.

Diante desse cenário, o mapeamento de áreas suscetíveis a inundações configura-se como uma ferramenta estratégica para subsidiar ações preventivas, políticas públicas e a tomada de decisão por órgãos de defesa civil e gestores municipais.

---

## 🎯 Objetivo do Projeto

Desenvolver um mapa de suscetibilidade a inundações para o município de Foz do Iguaçu–PR, utilizando dados geoespaciais e algoritmos de aprendizado de máquina, de modo a identificar e classificar espacialmente as áreas com maior predisposição à ocorrência de eventos de inundação.

---

## 🧠 Metodologia

A metodologia adotada no projeto compreende as seguintes etapas principais:

1. **Coleta de dados geoespaciais**
   - Modelos Digitais de Elevação (MDE)
   - Imagens de satélite Sentinel-2
   - Índices ambientais e espectrais (NDVI, NDWI, NDBI, entre outros)

2. **Pré-processamento dos dados**
   - Padronização espacial e reprojeção
   - Tratamento de valores ausentes
   - Empilhamento multibanda de rasters
   - Conversão da estrutura raster para base tabular

3. **Construção da base amostral**
   - Pontos de ocorrência e não ocorrência de inundações
   - Integração com variáveis ambientais

4. **Treinamento e avaliação dos modelos**
   - Algoritmos utilizados:
     - Random Forest (RF)
     - Redes Neurais Artificiais (RNA)
   - Avaliação por métricas estatísticas, como AUC e matriz de confusão

5. **Geração do mapa final**
   - Predição da suscetibilidade pixel a pixel
   - Classificação temática em níveis de risco
   - Exportação do mapa final em formato GeoTIFF

---

## 📊 Principais Resultados

Os resultados obtidos indicaram desempenho superior do algoritmo **Random Forest**, que apresentou maior capacidade de generalização e estabilidade em comparação às Redes Neurais Artificiais.

O mapa final de suscetibilidade evidenciou que uma parcela significativa do território de Foz do Iguaçu apresenta condições favoráveis à ocorrência de inundações, especialmente em áreas:
- De baixa altitude
- Próximas a corpos hídricos
- Com alta impermeabilização do solo

Além disso, foi desenvolvida uma aplicação web demonstrativa que permite a consulta da suscetibilidade a partir de endereços, evidenciando o potencial prático da metodologia proposta.

---


---

## 📦 Arquivos Grandes e Git LFS

Devido ao elevado tamanho dos arquivos raster (`.tif`) e dos modelos treinados (`.pkl`), este repositório utiliza **Git Large File Storage (Git LFS)** para versionamento adequado desses dados.

Ao clonar o repositório, certifique-se de ter o Git LFS instalado:

```bash
git lfs install
git clone https://github.com/enzomanenteferreira/TCC-Suscetibilidade-Inundacoes.git


