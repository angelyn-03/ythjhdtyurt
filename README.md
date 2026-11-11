# Analise-forense-terravision-evelyn-lemes
# Análise Forense & Computação Gráfica - TerraVision / Google Earth

**Estudante:** Evelyn Kauany Lemes da Silva  
**Número:** 06  
**Turma:** 3°D - DS | **Turno:** Matutino | **3° Trimestre**  
**Disciplinas Integradas:** Computação Gráfica, Ciência de Dados & Engenharia de Software  
**Professora:** Angélica Neckel  
**Tema Designado:** 6. Zonas Desérticas e Camadas de Areia (Uniformes e Dunas)  
**Objeto de Estudo:** Análise Forense da Arquitetura de Software do TerraVision / Google Earth (Caso ART+COM vs. Google)

---

## 1. Ciência de Dados & Lógica Computacional (`script.py`)

Em sistemas geospaciais 3D em tempo real, renderizar todas as texturas em resolução máxima exigiria uma quantidade inviável de memória RAM e VRAM. O arquivo `script.py` simula o algoritmo de **Level of Detail (LoD)**, utilizando estruturas condicionais (`if`, `elif`, `else`) para dinamicamente segmentar o carregamento da malha conforme a altitude da câmera virtual.

### A. Mapeamento Lógico por Nível de Zoom
* **Baixa Resolução (`altitude > 10.000m`):** Retorna o mosaico macro-continental do deserto. A prioridade computacional é a velocidade de transmissão de rede e a visualização global das fronteiras desérticas.
* **Média Resolução (`1.000m <= altitude <= 10.000m`):** Carrega mosaicos regionais destacando o relevo de dunas, vales de areia e cristas de grande porte. Reduz a sobrecarga de renderização enquanto o usuário navega em altitude intermediária.
* **Alta Resolução (`altitude < 1.000m`):** Renderiza texturas finas de alta definição, permitindo a visualização de micro-dunas, ondulações provocadas pelo vento e pequenas variações topográficas do terreno árido.

### B. Correlação Forense com o Caso TerraVision
A perícia de código realizada no julgamento demonstrou que a requisição em pirâmide de blocos geográficos (*tile pyramid streaming*) baseada em coordenadas condicionais e altitude era a ideia patenteada pela ART+COM. A lógica `if/else` implementada no `script.py` representa a base do algoritmo de otimização de dados geoespaciais disputado no tribunal.

---

## 2. Análise de Computação Gráfica & UX/UI

### A. Desafios de Processamento e Tratamento de Imagem
1. **Costura de Imagem (*Stitching*) e Algoritmos de Ajuste:**
   * **Desafio:** Regiões desérticas apresentam tom sobre tom (amarelo, bege, marrom) sem grandes pontos de referência contrastantes.
   * **Impacto em CG:** Algoritmos de busca por pontos de interesse (como SIFT ou SURF) falham ao tentar encontrar vértices idênticos em fotos de satélite adjacentes. Isso pode gerar costuras visíveis (*seams*) ou desalinhar dunas contínuas.
   * **Solução Técnica:** Aplicação de normalização de histograma e correção de cor multiespectral antes do alinhamento tridimensional.
2. **Sombreamento e Variação Fotométrica (*Shading & Exposure*):**
   * **Desafio:** Imagens de satélite capturadas em horários ou estações diferentes possuem incidências solares distintas.
   * **Impacto em CG:** Como dunas dependem diretamente do sombreamento (*shadow casting*) para demonstrar volume 3D, emendas de imagens com sombras em ângulos opostos quebram a ilusão tridimensional e a fidelidade forense da representação.

### B. Design de Interface & Leis da Gestalt
* **Lei da Continuidade:** As ondulações e cristas das dunas formam linhas fluídas na paisagem. O renderizador mantém a fidelidade dessas curvas contínuas durante a transição de textura (LoD), evitando que a troca de resolução cause saltos bruscos (*popping effect*) na percepção do usuário.
* **Lei da Figura-Fundo:** Devido à homogeneidade da areia (fundo), a interface do usuário (UI) e o renderizador projetam elementos de interesse — como estradas, formações rochosas, veículos ou oásis — com maior contraste (figura), orientando o foco de análise visual durante a navegação.
* **Lei do Fechamento:** O cérebro humano completa o desenho de cristas e formações desérticas interrompidas por áreas sem dados em alta resolução, garantindo navegação intuitiva mesmo quando o carregamento da rede oscila.

---

## 3. Evidências Visuais e Análise de Tela

![Mapeamento de Zona Desértica](deserto.png)  
*Figura 1: Captura de tela do Google Earth mapeando o terreno desértico, demonstrando a renderização da malha 3D de dunas e a aplicação do algoritmo de iluminação solar.*

---

## 4. Guia de Sustentação Técnica (Roteiro do Pitch Oral)

1. **Introdução (30s):** Apresente o tema de Zonas Desérticas e destaque que superfícies homogêneas são desafios clássicos para algoritmos de visão computacional e rendering.
2. **Lógica em Python (1min):** Explique como a função `carregar_camada_satelite` em `script.py` simula o carregamento condicional por altitude (`if/elif/else`) para economizar memória RAM/VRAM.
3. **Computação Gráfica & Gestalt (1min):** Explique o problema de *stitching* (costura) na areia, variação de sombras nas dunas e como as leis da Continuidade e Figura-Fundo facilitam a navegação do usuário.
4. **Conclusão (30s):** Finalize relacionando a otimização visual com o caso judicial do TerraVision vs. Google.
