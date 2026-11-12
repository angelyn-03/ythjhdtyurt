# RELATÓRIO DE ANÁLISE FORENSE COMPUTACIONAL E COMPUTAÇÃO GRÁFICA

### Estudo de Caso: A Batalha Bilionária — O Caso Google Earth (ART+COM e TerraVision)

---

## 1. IDENTIFICAÇÃO ACADÊMICA

- **Instituição:** Ensino Médio Técnico em Desenvolvimento de Sistemas
- **Disciplinas Integradas:** Front-End, Computação Gráfica, UX/UI, Banco de Dados, Lógica Computacional e de Programação, Ciência de Dados, Engenharia de Software e Análise Forense Computacional.
- **Docente Responsável:** Prof.ª Angélica Neckel
- **Discente:** Evelyn Kauany Lemes da Silva
- **Número:** 06
- **Turma:** 3.º D — Matutino
- **Tema de Sensoriamento Remoto:** Tema 6 — Zonas Desérticas e Camadas de Areia (Uniformes e Dunas).
- **Estudo de Caso:** TerraVision (ART+COM) vs. Google Earth.
- **Data de Submissão:** 16 de novembro de 2026.

---

## 2. CONTEXTUALIZAÇÃO HISTÓRICA E ANÁLISE FORENSE COMPUTACIONAL

A minissérie *A Batalha Bilionária: O Caso Google Earth*, baseada em acontecimentos reais, apresenta a disputa entre a empresa alemã ART+COM e a corporação Google envolvendo o desenvolvimento do TerraVision e a tecnologia de visualização geográfica.

O estudo permite relacionar os acontecimentos apresentados nos episódios com os conhecimentos desenvolvidos nas disciplinas de Ciência de Dados, Computação Gráfica, Engenharia de Software e Análise Forense Computacional.

### 2.1. Episódio 1 — A Ideia e o Protótipo

**Contextualização:**

O primeiro episódio apresenta as origens do TerraVision em Berlim, mostrando a criação do projeto, sua identidade visual, a modelagem do planeta e os primeiros desafios relacionados à manipulação de grandes volumes de dados geográficos.

**Relação com Ciência de Dados:**

- Visualização de dados e storytelling.
- Introdução à linguagem Python.
- Manipulação e organização de estruturas de dados.
- Conhecimento de bibliotecas e bases de dados.
- Análise exploratória de dados geográficos.

**Relação com Computação Gráfica:**

- Criação e refinamento da identidade visual.
- Construção de elementos gráficos e logotipo.
- Tratamento de imagens e texturas de satélite utilizando GIMP.
- Organização dos elementos gráficos na interface de usuário.

### 2.2. Episódio 2 — A Apresentação e o Algoritmo

**Contextualização:**

O segundo episódio apresenta a viagem ao Vale do Silício e a demonstração do TerraVision para a empresa Silicon Graphics (SGI), destacando os desafios de otimização de código, processamento de dados e utilização de imagens em alta resolução.

**Relação com Ciência de Dados:**

- Operações entre arrays e matrizes.
- Utilização de estruturas de repetição.
- Tratamento e filtragem de dados.
- Manipulação de informações conforme os níveis de zoom.
- Utilização de bibliotecas e funções para otimização de operações.

**Relação com Computação Gráfica:**

- Aplicação dos princípios da Gestalt.
- Tipografia e ambientação visual.
- Iluminação, cores e luminosidade.
- Processamento de imagens RAW.
- Representação visual da transição entre diferentes escalas geográficas.

### 2.3. Episódio 3 — O Lançamento do Google Earth e o Plágio

**Contextualização:**

O terceiro episódio aborda o surgimento do Google Earth e a controvérsia envolvendo as semelhanças entre as tecnologias utilizadas pelo Google e o sistema desenvolvido anteriormente pela ART+COM.

**Relação com Ciência de Dados:**

- Regressão linear com Scikit-Learn.
- Modelagem estatística e análise preditiva.
- Tratamento de exceções.
- Construção e interpretação de gráficos.
- Comparação de métricas e desempenho de sistemas.

**Relação com Computação Gráfica:**

- Padronização da identidade visual.
- Comparação de mockups.
- Análise das interfaces e da experiência do usuário (UX/UI).
- Criação de iluminação e ajuste de exposição.
- Renderização e sombreamento de modelos tridimensionais.

### 2.4. Episódio 4 — O Julgamento do Tribunal de Patentes

**Contextualização:**

O quarto episódio apresenta a disputa judicial, a análise técnica do código e a discussão sobre a propriedade intelectual relacionada ao TerraVision.

**Relação com Ciência de Dados:**

- Estruturas condicionais (`if`, `elif` e `else`).
- Exploração e análise de dados.
- Análise de código e investigação computacional.
- Visualização de informações e storytelling para apresentação de evidências técnicas.

**Relação com Computação Gráfica:**

- Exportação de arquivos e compatibilidade de formatos.
- Preparação de materiais gráficos.
- Criação de infográficos e apresentações visuais.
- Organização de evidências para facilitar a compreensão das informações técnicas.

### 2.5. Relação entre o Estudo de Caso e a Atividade

A análise dos episódios permite compreender que sistemas de visualização geográfica dependem da integração entre programação, processamento de imagens, estruturas de dados e recursos gráficos.

No desenvolvimento desta atividade, a lógica condicional é utilizada para simular a seleção de camadas de imagens conforme a altitude da câmera virtual.

Essa estratégia permite representar diferentes níveis de detalhamento sem exigir o carregamento de todas as informações em alta resolução simultaneamente.

---

## 3. CIÊNCIA DE DADOS E LÓGICA DE PROGRAMAÇÃO

### 3.1. Objetivo do Algoritmo

Em sistemas de visualização geográfica, como TerraVision e Google Earth, carregar todas as imagens do planeta em alta resolução pode consumir recursos desnecessários de memória RAM e VRAM.

Para otimizar o processamento, utiliza-se o conceito de **Level of Detail (LoD)**, que permite selecionar o nível de detalhamento das imagens conforme a altitude aproximada da câmera virtual.

O objetivo da implementação em Python é desenvolver uma função chamada:

`carregar_camada_satelite(lista_altitudes)`

A função recebe uma lista de altitudes em metros e utiliza estruturas condicionais para identificar qual camada de visualização deve ser carregada.

### 3.2. Classificação dos Níveis de Detalhamento

**LoD 0 — Baixa Resolução**

- Condição: altitude superior a 10.000 metros.
- Camada: mosaico geral da Terra.
- Elemento representado: visão ampla das regiões desérticas, grandes extensões de areia e localização geográfica do deserto.
- Objetivo computacional: reduzir a quantidade de detalhes processados durante a visualização em escala planetária.

**LoD 1 — Média Resolução**

- Condição: altitude entre 1.000 e 10.000 metros, incluindo os limites.
- Camada: mosaico regional do tema designado.
- Elemento representado: campos de dunas, extensões de areia, terrenos rochosos e características topográficas.
- Objetivo computacional: apresentar informações intermediárias sobre a distribuição e a formação do relevo desértico.

**LoD 2 — Alta Resolução**

- Condição: altitude inferior a 1.000 metros.
- Camada: detalhes finos do tema designado.
- Elemento representado: pequenas dunas, ondulações provocadas pelo vento, texturas da areia e irregularidades do terreno.
- Objetivo computacional: proporcionar maior detalhamento visual durante a aproximação da câmera.

### 3.3. Aplicação das Estruturas Condicionais

A lógica de programação utiliza estruturas condicionais para verificar os valores recebidos pela função.

- `if`: verifica se a altitude é superior a 10.000 metros.
- `elif`: verifica se a altitude está entre 1.000 e 10.000 metros.
- `else`: identifica altitudes inferiores a 1.000 metros.

A utilização dessas estruturas permite que o sistema escolha a camada de visualização correspondente a cada altitude.

### 3.4. Iteração e Processamento dos Dados

A função deve percorrer todos os valores presentes na lista de altitudes, utilizando uma estrutura de repetição.

Cada valor representa uma posição diferente da câmera virtual durante o processo de aproximação do terreno.

O algoritmo deve apresentar uma mensagem específica para cada nível de detalhamento, considerando o tema de zonas desérticas e camadas de areia.

### 3.5. Relação com a Computação Gráfica

O controle de detalhamento está relacionado à otimização da renderização tridimensional.

Quanto maior a aproximação da câmera, maior será a necessidade de apresentar detalhes da superfície.

No cenário desértico, isso significa passar de uma representação ampla do território para uma visualização regional das dunas e, posteriormente, para detalhes das texturas e ondulações da areia.

---

## 4. COMPUTAÇÃO GRÁFICA E PROCESSAMENTO DE IMAGENS

### 4.1. Características Visuais das Zonas Desérticas

O cenário escolhido apresenta características específicas que influenciam diretamente o processamento de imagens e a renderização tridimensional.

Entre elas estão:

- Predominância de tons bege, amarelos e terracota.
- Grandes superfícies de areia com pouca variação cromática.
- Formação de dunas com diferentes alturas e inclinações.
- Presença de sombras provocadas pela iluminação solar.
- Texturas naturais formadas pela ação do vento.
- Regiões rochosas com características visuais diferentes das áreas arenosas.

Essas características representam desafios para os sistemas de mapeamento e visualização geográfica.

### 4.2. Desafios de Stitching e Uniformização de Imagens

O *stitching* é o processo de unir diferentes imagens para formar uma representação visual contínua de determinada região geográfica.

No ambiente desértico, esse processo apresenta algumas dificuldades.

**Baixa variação cromática:**

A predominância de cores semelhantes pode dificultar a identificação de pontos de referência entre imagens de satélite.

Algoritmos de identificação de características visuais, como SIFT e SURF, podem apresentar dificuldades quando existem poucos elementos de contraste para estabelecer correspondências.

**Diferenças de iluminação:**

Imagens capturadas em horários diferentes podem apresentar variações de luminosidade e sombreamento.

Essas diferenças podem provocar descontinuidades visuais durante a união das imagens.

**Texturas homogêneas:**

Grandes áreas de areia podem apresentar padrões semelhantes, dificultando o alinhamento preciso dos fragmentos de imagem.

### 4.3. Iluminação, Sombreamento e Texturas

A iluminação solar é um elemento importante para a representação visual do relevo desértico.

As dunas apresentam diferentes inclinações e formatos, produzindo áreas iluminadas e regiões de sombra.

Essas variações ajudam o usuário a perceber a profundidade e a tridimensionalidade do terreno.

Entre os recursos relacionados à computação gráfica, destacam-se:

- **Shading:** técnica utilizada para representar a iluminação e o sombreamento das superfícies.
- **Normal Mapping:** recurso utilizado para simular detalhes de relevo por meio de informações de orientação das superfícies.
- **Filtragem anisotrópica:** técnica que melhora a visualização de texturas observadas em ângulos inclinados.
- **Normalização de histogramas:** procedimento que pode auxiliar na uniformização da distribuição de luminosidade entre imagens.

### 4.4. Aplicação dos Recursos nos Níveis de LoD

| Nível | Representação gráfica | Características |
|---|---|---|
| LoD 0 | Visão geral do deserto | Grandes extensões territoriais |
| LoD 1 | Campos de dunas | Relevo e formações arenosas |
| LoD 2 | Detalhamento da superfície | Texturas, pequenas ondulações e sombras |

A utilização desses níveis permite adaptar a quantidade de detalhes exibidos conforme a distância da câmera virtual.

---

## 5. DESIGN DE INTERFACE E LEIS DA GESTALT (UX/UI)

As Leis da Gestalt são princípios da percepção visual que ajudam a compreender como os usuários organizam e interpretam os elementos apresentados em uma interface.

Em sistemas como o Google Earth, esses princípios contribuem para facilitar a identificação de regiões geográficas e orientar a navegação durante a aproximação do terreno.

### 5.1. Lei da Figura-Fundo

A Lei da Figura-Fundo estabelece a distinção entre o elemento principal de interesse e o ambiente que funciona como plano de fundo.

**Aplicação no cenário desértico:**

As dunas, formações rochosas, construções e oásis podem ser percebidos como elementos principais, enquanto as grandes extensões de areia funcionam como fundo visual.

**Contribuição para a navegação:**

A diferenciação visual facilita a identificação dos elementos geográficos e ajuda o usuário a direcionar sua atenção para as regiões que deseja observar.

### 5.2. Lei da Continuidade

A Lei da Continuidade está relacionada à tendência humana de acompanhar visualmente linhas, formas e padrões que apresentam uma sequência organizada.

**Aplicação no cenário desértico:**

As cristas das dunas apresentam formas curvilíneas e contínuas, que podem ser acompanhadas visualmente durante a observação do terreno.

**Contribuição para a navegação:**

A continuidade visual facilita a percepção do relevo durante a aproximação da câmera, contribuindo para uma experiência de navegação mais fluida entre diferentes níveis de detalhamento.

### 5.3. Lei da Proximidade

A Lei da Proximidade determina que elementos visualmente próximos tendem a ser percebidos como integrantes de um mesmo grupo.

**Aplicação no cenário desértico:**

Dunas próximas, formações rochosas e conjuntos de elementos geográficos podem ser interpretados como agrupamentos dentro da paisagem.

**Contribuição para a navegação:**

A organização espacial ajuda o usuário a identificar regiões com características semelhantes e compreender a distribuição dos elementos presentes no terreno.

### 5.4. Lei do Fechamento

A Lei do Fechamento está relacionada à capacidade humana de completar mentalmente formas e estruturas que apresentam partes incompletas.

**Aplicação no cenário desértico:**

Mesmo quando partes de uma imagem ainda não foram carregadas, o usuário pode reconhecer padrões de continuidade nas formações das dunas e na disposição do terreno.

**Contribuição para a navegação:**

Esse princípio auxilia a interpretação visual do ambiente, mesmo quando existem pequenas interrupções ou lacunas na representação gráfica.

### 5.5. Experiência do Usuário e Navegação por Zoom

A interface de um sistema de visualização geográfica precisa permitir que o usuário compreenda sua localização e consiga aproximar ou afastar a câmera de maneira intuitiva.

No cenário desértico, a navegação por zoom permite observar diferentes características da superfície:

1. Na visão distante, o usuário identifica a extensão territorial do deserto.
2. Na aproximação intermediária, consegue observar campos de dunas e formações rochosas.
3. Na aproximação elevada, pode analisar texturas, ondulações e pequenas irregularidades da areia.

A organização visual dos elementos, a continuidade do relevo e a diferenciação entre figura e fundo contribuem para uma experiência de navegação mais clara e intuitiva.

---

## 6. EVIDÊNCIA DE MAPEAMENTO GEOGRÁFICO E ANÁLISE DE IMAGEM

### 6.1. Registro Visual do Tema Designado

A imagem abaixo representa o cenário desértico utilizado como referência para a análise de computação gráfica e sensoriamento remoto.

![Deserto do Saara — evidência visual do cenário desértico](./deserto%20di%20saara.png)

*Figura 1 — Registro visual do ambiente desértico utilizado na análise de zonas desérticas e formações rochosas.*

### 6.2. Análise Técnica da Imagem

**1. Representação de Alta Resolução — LoD 2**

A aproximação da câmera permite observar elementos com maior nível de detalhamento, como estruturas arquitetônicas, formações rochosas, irregularidades do terreno e características da superfície.

No contexto do algoritmo proposto, essa representação corresponde ao nível de alta resolução.

**2. Análise de Iluminação e Sombreamento**

A incidência da iluminação solar produz áreas de luz e sombra nas superfícies.

Essas diferenças ajudam a identificar profundidade, volume e características tridimensionais das estruturas.

**3. Análise de Textura e Uniformidade**

A predominância de tons amarelados, beges e terracota demonstra como superfícies visualmente semelhantes podem representar dificuldades para o alinhamento e a uniformização de imagens.

**4. Aplicação das Leis da Gestalt**

- **Figura-Fundo:** as estruturas e formações rochosas destacam-se em relação ao ambiente ao redor.
- **Continuidade:** as linhas arquitetônicas e as formas do relevo conduzem a percepção visual.
- **Proximidade:** elementos próximos podem ser interpretados como partes de um mesmo conjunto.

### 6.3. Relação com o Sensoriamento Remoto

O sensoriamento remoto permite obter informações sobre a superfície terrestre por meio de imagens capturadas por sensores instalados em satélites e outras plataformas.

No estudo das zonas desérticas, essas imagens permitem observar:

- Distribuição das áreas arenosas.
- Formações e padrões de dunas.
- Características das superfícies rochosas.
- Variações de textura e luminosidade.
- Alterações visuais na paisagem.

A análise dessas informações contribui para compreender como os sistemas de visualização geográfica representam diferentes tipos de terreno.

---

## 7. ESTRUTURA DO PROJETO NO GITHUB

O repositório foi organizado para apresentar o código desenvolvido em Python e a documentação técnica da atividade.

### 7.1. Organização dos Arquivos

```text
analise-forense-terravision-evelyn/
│
├── README.md
│
├── script.py
│
└── deserto di saara.png
```

**README.md:** contém a identificação acadêmica, contextualização histórica, explicações técnicas, análise de processamento de imagens, aplicação das Leis da Gestalt e evidências visuais.

**script.py:** contém a função `carregar_camada_satelite(lista_altitudes)`, desenvolvida em Python para classificar as altitudes e selecionar os níveis de detalhamento.

**deserto di saara.png:** arquivo de imagem utilizado como referência visual do cenário desértico.

### 7.2. Versionamento com Git e GitHub

O Git permite acompanhar as modificações realizadas nos arquivos durante o desenvolvimento do projeto.

O GitHub permite armazenar o repositório remotamente, organizar os arquivos e disponibilizar o trabalho publicamente.

O histórico de commits deve apresentar mensagens claras e relacionadas às alterações realizadas.

Exemplos de mensagens de commits:

- `Initial commit: estrutura inicial do projeto`
- `Add: implementação do algoritmo de níveis LoD`
- `Add: documentação do relatório técnico`
- `Add: imagem do cenário desértico`
- `Update: análise de computação gráfica e UX/UI`

---

## 8. SUSTENTAÇÃO TÉCNICA — PITCH ORAL

A apresentação individual terá duração aproximada de 2 a 3 minutos, conforme as orientações da professora.

### 8.1. Introdução Técnica

Apresentação do tema escolhido e explicação da importância da computação gráfica na representação de ambientes geográficos.

O cenário selecionado corresponde às zonas desérticas e camadas de areia, que apresentam características específicas de textura, iluminação e formação de dunas.

### 8.2. Fundamentação de Ciência de Dados

Explicação da função `carregar_camada_satelite(lista_altitudes)` e da utilização das estruturas condicionais `if`, `elif` e `else`.

Apresentação dos três níveis de detalhamento:

- LoD 0: baixa resolução.
- LoD 1: média resolução.
- LoD 2: alta resolução.

Demonstração de como a altitude influencia a escolha da camada de visualização.

### 8.3. Análise de Computação Gráfica

Apresentação dos principais desafios relacionados ao processamento de imagens de ambientes desérticos, como:

- Baixa variação cromática.
- Dificuldades de stitching.
- Diferenças de iluminação.
- Sombreamento das dunas.
- Representação das texturas arenosas.

Explicação das Leis da Gestalt identificadas na organização visual e na navegação por zoom.

### 8.4. Conclusão

Finalização destacando a importância da integração entre Ciência de Dados, Lógica de Programação e Computação Gráfica para o desenvolvimento de sistemas de visualização geográfica.

---

## 9. CONSIDERAÇÕES FINAIS

O desenvolvimento desta atividade permite compreender a importância da integração entre diferentes áreas da tecnologia na construção de sistemas de visualização geográfica.

A análise do caso TerraVision e sua relação com o Google Earth possibilita observar como a programação, a manipulação de dados e a computação gráfica estão presentes na representação digital do planeta.

O estudo das zonas desérticas demonstra que a baixa variação cromática, as texturas homogêneas, a iluminação solar e as formações de dunas representam desafios específicos para o processamento e a renderização de imagens.

A utilização dos níveis de detalhamento LoD permite compreender como a altitude da câmera virtual influencia a seleção das informações visuais apresentadas ao usuário.

Além disso, a aplicação das Leis da Gestalt demonstra como os princípios da percepção visual contribuem para organizar os elementos gráficos e facilitar a navegação em interfaces geográficas.

Conclui-se que a integração entre Ciência de Dados, Lógica de Programação, Computação Gráfica e UX/UI é fundamental para o desenvolvimento e a compreensão de sistemas modernos de visualização geográfica.

---

**TRABALHO ACADÊMICO — DESENVOLVIMENTO DE SISTEMAS**

**Discente:** Evelyn Kauany Lemes da Silva

**Turma:** 3.º D — Matutino

**Docente:** Prof.ª Angélica Neckel 
