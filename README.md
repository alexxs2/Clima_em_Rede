Projeto da disciplina de Processamento de Linguagem Natural (PLN) 
# Autores:
- **Andressa dos santos Silva**
- **Alexsandro Da Silva Bezerra**
- **Alexandre Da Cunha Fernandes**
- **Breno Henrique Reys Lorenzo**
- **Leonardo De Jesus Andrade**
- **Raphael Imperator Cavicchia Fleury**

# **Clima em Rede: Análise de Grafos Climáticos em Notícias 🌎**
**INTRODUÇÃO**

nos últimos anos, as discussões sobre clima têm ganhado força em grandes centros urbanos como São Paulo, refletindo preocupações crescentes com mudanças climáticas, qualidade do ar e eventos extremos.

**OBJETIVO**

O objetivo era construir e analisar grafos de co-ocorrência de palavras a partir de notícias sobre clima no portal G1 (2022‑2024), identificando padrões semânticos, tópicos recorrentes e comunidades de termos inter-relacionados.

🛠️ **Ferramentas & Bibliotecas**

**Python**
- Web Scraping: requests, BeautifulSoup
- PLN: spaCy (tokenização, lematização, stopwords)
- Grafos: NetworkX
- Manipulação Numérica: NumPy
 - Visualização: Matplotlib

⚙️ **METODOLOGIA**

Desenvolvemos um conjunto de funções para automatizar cada etapa:

**Coleta de Dados**

```coletar_texto(url)```: faz scraping das notícias no G1, extraindo o texto principal.

**Processamento de Texto**

Pipeline em spaCy para tokenização, lematização e remoção de stopwords.

Filtragem por vocabulário climático (e.g., “chuva”, “vento”, “granizo”).

**Construção de Grafos**

```construir_grafo(texto)```: cria um grafo de co-ocorrência com janela deslizante de tamanho 2, atribuindo peso às arestas conforme a frequência dos pares 
de palavras.

**Estatística**

```estatisticas_grafo(G)```: calcula número de nós/arestas, graus, centralidade de intermediação, coeficiente de agrupamento médio e modularidade.

**Visualização**

```plotar_grafo(G)```: gera diagramas com layout de força (spring), colorindo comunidades detectadas pelo algoritmo de modularidade.

🔍 **Principais Insights**

Termos Centrais: “temperatura”, “chuva”, “calor” e “recorde” aparecem com bem mais frequência , indicando foco em variações e extremos climáticos.

Comunidades Temáticas: agrupamentos revelam subtemas como riscos de alagamentos, sensação térmica e fenômenos sazonais (rajadas, nebulosidade).

Evolução Temporal: redução na ênfase em “chuva” (2022→2024) e aumento de palavras relacionadas à intensidade e recordes de calor, sugerindo maior preocupação com impactos dos eventos climáticos ao decorrer desses anos.

Fonte das Notícias: https://g1.globo.com
