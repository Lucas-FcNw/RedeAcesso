# UNIVERSIDADE PRESBITERIANA MACKENZIE
## Faculdade de Computação e Informática
**Disciplina:** Teoria dos Grafos — Turma 6G  
**Professor:** Dr. Ivan Carlos Alcântara de Oliveira  
**Projeto da Disciplina — Parte 2**

---

## 1) Dados dos integrantes do grupo

- Lucas Fernandes de Camargo — RA 10419400
- Lendy Naiara Carpio Pacheco — RA 10428525
- Anna Luiza Stella Santos — RA 10417401

> Requisito “grupo de até 3 pessoas”: **atendido**.

## 2) Título provisório da aplicação

**SPGraph — Análise de Acesso Territorial a Serviços de Saúde em São Paulo**

## 3) Introdução

Este relatório apresenta os resultados da Atividade Projeto — Parte 2, com foco na modelagem de um problema real por Teoria dos Grafos e implementação de uma aplicação em Python para leitura, gravação e manipulação de grafos no formato exigido pela disciplina.

A solução foi construída com lista de adjacência e menu textual (`a` até `j`), cobrindo as operações obrigatórias e a análise de conectividade do grafo.

## 4) Definição do problema real selecionado (descrição detalhada)

### 4.1 Contexto

A distribuição espacial de serviços de saúde no município de São Paulo não é uniforme. Isso gera diferenças de acesso entre distritos, especialmente quando se considera conectividade territorial e distância entre regiões.

### 4.2 Formulação em grafos

- **Vértices:** distritos administrativos de São Paulo.
- **Arestas:** adjacências geográficas entre distritos.
- **Peso de vértice:** população do distrito.
- **Peso de aresta:** distância estimada (km) entre distritos adjacentes.

### 4.3 Tipo do grafo utilizado

No arquivo [grafo.txt](grafo.txt), foi utilizado:

- **Tipo 3** — grafo **não orientado** com **peso nos vértices e nas arestas**.

### 4.4 Escala final da modelagem

- Número de vértices: **71**
- Número de arestas: **215**

Validação dos mínimos exigidos no enunciado:

- $71 \ge 70$ vértices ✅
- $215 \ge 180$ arestas ✅

### 4.5 Vinculação explícita com ODS (Saúde e Desigualdade)

Este projeto está diretamente alinhado com duas frentes da Agenda 2030:

- **ODS 3 — Saúde e Bem-Estar**
- **ODS 10 — Redução das Desigualdades**

No recorte do problema, a cidade é representada por distritos (vértices) e conexões territoriais (arestas), permitindo analisar diferenças de acesso à saúde entre regiões. Assim, a modelagem não trata apenas de distância geográfica, mas também de desigualdade territorial de acesso a serviços essenciais.

Contribuição para a **ODS 3**:

- evidencia a estrutura de acesso territorial a serviços de saúde;
- permite identificar regiões potencialmente mais vulneráveis por baixa conectividade;
- fornece base analítica para priorização de ações em saúde pública.

Contribuição para a **ODS 10**:

- torna comparável o acesso entre distritos com diferentes condições urbanas;
- mostra assimetrias de conectividade e deslocamento entre áreas da cidade;
- apoia decisões voltadas à redução de desigualdades no atendimento à população.

Em síntese, o grafo modelado funciona como instrumento técnico para observar e comunicar desigualdades de acesso à saúde, conectando o problema real selecionado às metas de saúde e equidade social.

## 5) Estudo de caso com dados reais

Bases de dados reais usadas na preparação do modelo:

- `deinfosacadsau2014.csv` (serviços de saúde e leitos)
- `evolucao_msp_pop_sexo_idade.csv` (população por distrito)

Recorte territorial aplicado para viabilização no prazo acadêmico:

- zonas mantidas: **Leste, Norte e Sul**.

## 6) Modelagem no Graph Online / software similar e imagem relacionada

### 6.1 Imagem da modelagem na ferramenta

![Modelagem no software (versão final)](figuras/swappy-20260402-212746.png)

### 6.2 Imagem do grafo resultante

![Visão geral do grafo](figuras/01_visao_geral_grafo.png)

### 6.3 Imagens técnicas complementares

![Distribuição de grau](figuras/02_histograma_graus.png)

![Matriz de adjacência](figuras/03_matriz_adjacencia.png)

## 7) Métricas estruturais do grafo

Fonte: [figuras/metricas.json](figuras/metricas.json)

- Tipo: 3 (não orientado, ponderado)
- Vértices: 71
- Arestas: 215
- Grau médio: 6.06
- Grau máximo: 11
- Grau mínimo: 1
- Densidade: 0.0865
- Conexidade: **conexo** (1 componente)

## 8) Desenvolvimento da aplicação com menu de opções (a-j)

Arquivo principal: [projeto_grafo_menu.py](projeto_grafo_menu.py)

Funcionalidades implementadas conforme enunciado:

- `a)` Ler dados do arquivo `grafo.txt`
- `b)` Gravar dados no arquivo `grafo.txt`
- `c)` Inserir vértice
- `d)` Inserir aresta
- `e)` Remover vértice
- `f)` Remover aresta
- `g)` Mostrar conteúdo do arquivo
- `h)` Mostrar grafo (lista de adjacência)
- `i)` Apresentar a conexidade do grafo e o reduzido
- `j)` Encerrar aplicação

Observação técnica relevante:

- Para grafo não orientado (tipo 3), a opção `i` informa conectividade (conexo/desconexo).
- A parte de “reduzido” foi validada adicionalmente com um grafo direcionado de teste.

## 9) Objetivos ODS contemplados e justificativa

### ODS 3 — Saúde e Bem-Estar
O tema central do projeto é acesso territorial a serviços de saúde, conectando diretamente a modelagem ao objetivo de saúde e bem-estar.

### ODS 10 — Redução das Desigualdades
A análise por grafos evidencia diferenças regionais de conectividade e acesso, apoiando leitura de desigualdades territoriais.

### ODS 11 — Cidades e Comunidades Sustentáveis
Os resultados podem apoiar planejamento urbano e melhor distribuição territorial de serviços públicos essenciais.

## 10) Printscreen de testes da execução do menu (mínimo: 2 por opção)

Evidências textuais consolidadas:

- [evidencias/testes_menu.txt](evidencias/testes_menu.txt)
- [evidencias/teste_i2_direcionado.txt](evidencias/teste_i2_direcionado.txt)
- [evidencias/validacao_grafo.txt](evidencias/validacao_grafo.txt)

### 10.1 Galeria completa de imagens (todas as imagens da entrega)

#### Imagens técnicas da modelagem

![Visão geral do grafo](figuras/01_visao_geral_grafo.png)

![Histograma de graus](figuras/02_histograma_graus.png)

![Matriz de adjacência](figuras/03_matriz_adjacencia.png)

#### Prints coletados da execução/modelagem

![Print da modelagem final](figuras/swappy-20260402-212746.png)

![Print 1](figuras/img1.png)

![Print 2](figuras/img2.png)

![Print 3](figuras/img3.png)

![Print 4](figuras/img4.png)

![Print 5](figuras/img5.png)

### 10.2 Checklist de cobertura dos testes (2 por item)

- `a1`, `a2` — leitura válida e inválida.
- `b1`, `b2` — gravação padrão e gravação em nome alternativo.
- `c1`, `c2` — inserção de novo vértice e tentativa de duplicado.
- `d1`, `d2` — inserção de aresta válida e inválida.
- `e1`, `e2` — remoção de vértice existente e inexistente.
- `f1`, `f2` — remoção de aresta existente e inexistente.
- `g1`, `g2` — exibição de conteúdo de arquivo existente e inexistente.
- `h1`, `h2` — lista de adjacência com arquivo carregado e sem carregar.
- `i1`, `i2` — conectividade em não orientado e categoria/reduzido em direcionado de teste.
- `j1`, `j2` — encerramento imediato e encerramento após operações.

## 11) Conformidade com os itens obrigatórios do enunciado

### 11.1 Relatório completo (Template)

- Dados dos integrantes: **atendido**.
- Título provisório da aplicação: **atendido**.
- Introdução + problema real detalhado + modelagem + imagem: **atendido**.
- ODS com justificativa: **atendido**.
- Prints de testes do menu (2 por opção): **atendido** (com evidências textuais e prints coletados).
- Apêndice com link do GitHub: **atendido**.

### 11.2 Conteúdo obrigatório no GitHub público

- Relatório do projeto: **atendido**.
- Arquivo `grafo.txt`: **atendido**.
- Arquivos fonte com cabeçalho (integrantes, síntese, histórico): **atendido**.
- Documentação interna/comentários: **atendido**.

## 12) Itens operacionais da entrega e apresentação

Itens dependentes de ação da equipe no AVA/sala:

- envio no AVA por um integrante;
- submissão no prazo oficial;
- apresentação em sala (até 5 minutos, com todos os integrantes presentes).

## 13) Apêndice — Link do projeto no GitHub

Repositório público:

- https://github.com/Lucas-FcNw/Programming

Caminho da entrega:

- `Python/Projetos/Grafos/entrega_parte2`

## 14) Conclusão

A Entrega Parte 2 foi finalizada com aderência ao enunciado: problema real modelado por grafo, escala mínima atendida, arquivo [grafo.txt](grafo.txt) no padrão exigido, aplicação funcional em Python com menu completo (`a` a `j`), validação de conectividade e documentação técnica com evidências de execução.
