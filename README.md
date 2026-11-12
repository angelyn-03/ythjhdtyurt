# RELATÓRIO DE ANÁLISE FORENSE COMPUTACIONAL E COMPUTAÇÃO GRÁFICA
### Estudo de Caso: Algoritmo TerraVision (ART+COM) vs. Google Earth

**Instituição:** Ensino Médio Técnico em Desenvolvimento de Sistemas  
**Disciplinas Integradas:** Computação Gráfica, Ciência de Dados, Engenharia de Software, Lógica de Programação e Análise Forense Computacional  
**Docente Responsável:** Prof.ª Angélica Neckel  
**Discente:** Evelyn Kauany Lemes da Silva | **N.º:** 06 | **Turma:** 3.º D — Matutino  
**Tema de Sensoriamento Remoto Designado:** Tema 6 — Zonas Desérticas e Camadas de Areia (Uniformes e Dunas)  
**Data de Submissão:** 16 de Novembro de 2026  

---

## 1. Contextualização Histórica e Perícia Forense (A Minissérie)

A controvérsia jurídica retratada no tribunal de Delaware entre a empresa alemã ART+COM e a corporação Google fundamentou-se na prioridade de patente sobre o algoritmo de *streaming* de dados geoespaciais em tempo real. Conforme abordado no **Episódio 2 (O Algoritmo)** e no **Episódio 4 (O Julgamento Final)**:

* **Inovação Técnica da ART+COM:** O software *TerraVision* introduziu o conceito de representação multinível do planeta Terra (*tile pyramid streaming*), requisitando fragmentos de imagens dinamicamente de acordo com as coordenadas do usuário e a altitude da câmera virtual.
* **Quebra Forense de Código:** A auditoria computacional apresentada em juízo demonstrou que a otimização de memória por meio de estruturas condicionais encadeadas (`if/elif/else`) constituía a espinha dorsal lógica para viabilizar a navegação fluída sem sobrecarregar a memória VRAM das estações de trabalho da época.

---

## 2. Ciência de Dados e Lógica de Programação (`script.py`)

No escopo da disciplina de Ciência de Dados, a manipulação de grandes volumes de dados espaciais exige estratégias estritas de otimização de infraestrutura de hardware. O script em linguagem Python (`script.py`) simula o mecanismo de **Level of Detail (LoD)** empregado pelos motores de renderização 3D.

### A. Algoritmo de Controle por Altitude
O processamento condicional classifica a aproximação da câmera virtual em três patamares hierárquicos:

1. **Baixa Resolução ($\text{Altitude} > 10.000\,\text{m}$ — LoD 0):**
   * *Ação:* Requisição do mosaico macro-continental desértico.
   * *Foco Computacional:* Minimização da amostragem poligonal e economia de largura de banda de rede para renderização de escala planetária.
2. **Média Resolução ($1.000\,\text{m} \le \text{Altitude} \le 10.000\,\text{m}$ — LoD 1):**
   * *Ação:* Mapeamento regional topográfico dos campos de dunas (*ergs*) e maciços rochosos.
   * *Foco Computacional:* Carregamento de malhas tridimensionais intermediárias com aplicação de filtragem anisotrópica para preservação da textura em perspectiva.
3. **Alta Resolução ($\text{Altitude} < 1.000\,\text{m}$ — LoD 2):**
   * *Ação:* Renderização de alta fidelidade das micro-dunas, ondulações geradas pelo vento (*ripples*) e detalhamento tátil da areia.
   * *Foco Computacional:* Utilização de *Normal Mapping* e consumo de alta taxa de preenchimento (*fill rate*) da placa gráfica.

---

## 3. Computação Gráfica, Processamento de Imagens e UX/UI

### A. Desafios de Tratamento Fotométrico e Alinhamento de Imagens
* **Complexidade do *Stitching* em Superfícies Homogêneas:** O mapeamento de ecossistemas desérticos apresenta reduzida variação cromática (predominância de tons beges e amarelados). Algoritmos convencionais de detecção de pontos de interesse (como SIFT/SURF) enfrentam inconsistência na identificação de vértices correspondentes, aumentando a probabilidade de artefatos visíveis nas emendas de mosaicos de satélite.
* **Inconsistência Fotométrica e Sombra Dinâmica:** A percepção de relevo tridimensional em dunas de areia depende da incidência da iluminação solar. Imagens de satélite obtidas sob diferentes ângulos zenitais criam divergências de sombreamento (*shadow casting*), exigindo normalização de histogramas para evitar descontinuidade no modelo 3D.

### B. Aplicação das Leis da Gestalt na Interface de Usuário
* **Lei da Continuidade:** As cristas curvilíneas e contínuas das dunas são preservadas graficamente pelo motor de renderização durante a alternância entre níveis de LoD, assegurando a estabilidade visual e prevenindo o fenômeno de *popping* (transição abrupta de geometrias).
* **Lei da Figura-Fundo:** O design de interface tira proveito da uniformidade do terreno (areia atuando como matriz de fundo) para destacar vetores de interesse analítico, tais como oásis, vias de transporte e afloramentos rochosos (figuras de elevado contraste).
* **Lei do Fechamento:** Habilita a interpretação cognitiva da topografia continuada pelo operador da aplicação, mesmo diante de eventuais latências de rede no carregamento dos blocos de textura de alta definição.

---

## 4. Evidência de Mapeamento Geográfico

![Captura de tela do Google Earth](deserto di saara.png)  
*Figura 1: Mapeamento orbital de terreno árido via Google Earth. Observa-se a aplicação da renderização tridimensional de relevo, o sombreamento dinâmico de cristas e a manutenção da continuidade estrutural do solo.*

---

## 5. Estrutura do Relatório de Sustentação Técnica (Pitch Oral)

Para a defesa individual perante a banca examinadora, a sustentação oral observará o seguinte encadeamento analítico:

1. **Introdução Técnica (30 segundos):** Apresentação da estudante como analista e síntese dos desafios de computação gráfica na representação de terrenos de baixa variância cromática.
2. **Fundamentação de Ciência de Dados (60 segundos):** Explanação da função `carregar_camada_satelite` em Python, destacando como o controle por *hardware* via blocos condicionais se conecta à disputa de patentes do caso *TerraVision*.
3. **Análise de Computação Gráfica (60 segundos):** Diagnóstico das limitações de *stitching*, inconsistências fotométricas nas sombras das dunas e a aplicação das Leis da Gestalt na navegação.
4. **Síntese e Conclusão (30 segundos):** Considerações finais sobre a importância da arquitetura de software na viabilização de sistemas GIS (*Geographic Information Systems*) modernos.
