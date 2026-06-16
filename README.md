**UNICESUMAR – Universidade Cesumar**  
Programação Front End

*Atividade Prática Final — 2º Bimestre*

*![Título: Logomarca Conex - Descrição: Logomarca da Conex][image1]*

**DOCUMENTO DE REQUISITOS**

Projeto Conex — Landing Page Institucional

**Integrantes do grupo**

\[Enzo Dell’Agnolo\] — RA: \[25017806-2\]

\[José Carlos de Mello Junior\] — RA: \[25357053-2\]

\[Lauro Golemba Junior\] — RA: \[25362737-2\]

\[Matheus Romero Marin\] — RA: \[25361338-2\]

\[Renan Madeira Evaristo\] — RA: \[25011033-2\]

\[Samuel Felipe Narciso\] — RA: \[25247839-2\]

   
Turma: \[ADS3S-M-A\]

Professor: Esp. Dácio F. Machado

Maringá – PR, junho de 2026

**Sumário**

1\. Introdução.................................................................................................................. 1

1.1 Objetivo do documento........................................................................................ 1

1.2 Visão geral do projeto.......................................................................................... 1

1.3 Escopo.................................................................................................................. 1

2\. Descrição Geral......................................................................................................... 1

2.1 Contexto de negócio............................................................................................ 1

2.2 Público-alvo.......................................................................................................... 1

2.3 Estrutura da aplicação......................................................................................... 1

3\. Requisitos Funcionais (RF)....................................................................................... 1

4\. Requisitos Não-Funcionais (RNF)............................................................................. 1

5\. Recursos da Página (Features)................................................................................. 1

5.1 Cabeçalho e navegação...................................................................................... 1

5.2 Seção principal (Hero)......................................................................................... 1

5.3 Nossas Soluções (cards)..................................................................................... 1

5.4 Rastreamento....................................................................................................... 1

5.5 Contato................................................................................................................. 1

5.6 Rodapé................................................................................................................. 1

5.7 Página de Serviços.............................................................................................. 1

6\. Decisões de Layout e Interface................................................................................. 1

6.1 Identidade visual e logomarca............................................................................. 1

6.2 Paleta de cores.................................................................................................... 1

6.3 Tipografia.............................................................................................................. 1

6.4 Estrutura de layout............................................................................................... 1

6.5 Experiência do usuário (UX)................................................................................ 1

7\. Tecnologias Aplicadas (Stack).................................................................................. 1

7.1 Linguagens e técnicas......................................................................................... 1

7.2 Justificativa da escolha........................................................................................ 1

7.3 Estrutura de arquivos........................................................................................... 1

8\. Hospedagem (Deployment)....................................................................................... 1

9\. Limitações e Trabalhos Futuros................................................................................ 1

 

 

# **1\. Introdução**

## **1.1 Objetivo do documento**

Este documento de requisitos descreve a solução web desenvolvida para o projeto Conex, apresentando os recursos (features) implementados, as decisões de layout e interface adotadas e as tecnologias aplicadas (technology stack). Ele tem por finalidade registrar o escopo do trabalho, servir de referência para a avaliação e justificar as escolhas técnicas e de design realizadas pelo grupo.

## **1.2 Visão geral do projeto**

A Conex é uma empresa fictícia de comércio exterior especializada em logística de contêineres entre a China e o Brasil, oferecendo serviços de FCL (Full Container Load), consolidação LCL (Less than Container Load) e inspeção de carga. O projeto consiste em uma página web institucional (landing page) cujo objetivo é apresentar a empresa, comunicar seus serviços e oferecer canais de contato e rastreamento.

## **1.3 Escopo**

O escopo contempla o desenvolvimento front-end de uma aplicação web estática, composta por duas páginas integradas, com identidade visual própria, design responsivo (responsive) e interações em JavaScript. Recursos de back-end (envio real de e-mails, persistência de dados e integração com APIs de rastreamento) estão fora do escopo desta entrega e são tratados como simulações no lado do cliente (client-side).

# **2\. Descrição Geral**

## **2.1 Contexto de negócio**

O comércio com a China demanda confiança, agilidade e transparência logística. A Conex posiciona-se como ponte entre o importador e a indústria chinesa, com presença nos portos de Ningbo, Shanghai e Shenzhen. A página comunica esse posicionamento e direciona o visitante à solicitação de cotação.

## **2.2 Público-alvo**

Importadores, empresas de médio e grande porte e profissionais de comércio exterior interessados em soluções de transporte de contêineres e inspeção de fornecedores na China.

## **2.3 Estrutura da aplicação**

A aplicação é composta por duas páginas com cabeçalho e rodapé compartilhados:

•      **index.html** — página inicial (Home/Landing Page) com apresentação, serviços, rastreamento e contato.

•      **servicos.html** — página de detalhamento dos serviços (FCL, LCL e Inspeção de Carga).

# **3\. Requisitos Funcionais (RF)**

Os requisitos funcionais descrevem o que a aplicação faz, do ponto de vista do usuário.

| ID | Requisito | Descrição |
| :---- | :---- | :---- |
| **RF01** | Navegação | Menu fixo (sticky header) com links para as seções e páginas, e navegação por âncoras com rolagem suave (smooth scroll). |
| **RF02** | Apresentação institucional | Seção principal (hero) com proposta de valor da empresa e botões de chamada para ação (CTA): “Ver Serviços” e “Solicitar Cotação”. |
| **RF03** | Listagem de serviços | Exibição dos três serviços (FCL, LCL e Inspeção) em cartões (cards) com ícone, descrição resumida e link “Saiba mais”. |
| **RF04** | Detalhamento de serviços | Página dedicada com a descrição completa de cada serviço, acessível pelos links “Saiba mais” por meio de âncoras (\#fcl, \#lcl, \#inspecao). |
| **RF05** | Rastreamento de contêiner | Campo para informar o número do BL/Container e botão “Rastrear”. A consulta é simulada via JavaScript, com validação de campo vazio e retorno de mensagem ao usuário. |
| **RF06** | Formulário de contato | Formulário com nome, e-mail, tipo de serviço e mensagem. Possui validação nativa (atributo required) e feedback de envio simulado via JavaScript (sem back-end). |
| **RF07** | Identidade visual | Exibição da logomarca da Conex no cabeçalho (com link para a home) e como favicon nas abas do navegador. |

# **4\. Requisitos Não-Funcionais (RNF)**

Os requisitos não-funcionais descrevem atributos de qualidade da aplicação.

| ID | Categoria | Requisito |
| :---- | :---- | :---- |
| **RNF01** | Responsividade | Layout adaptável a celular, tablet e desktop, utilizando CSS Grid, Flexbox e media queries (breakpoints em 768px e 1024px). |
| **RNF02** | Acessibilidade | Rótulos (labels) associados aos campos de formulário, ícones decorativos marcados com aria-hidden, idioma definido (lang="pt-BR") e texto alternativo (alt) na logomarca. |
| **RNF03** | Desempenho | Páginas estáticas e leves, sem dependências externas nem framework, com imagens otimizadas e folha de estilo única compartilhada — favorecendo o carregamento rápido. |
| **RNF04** | Compatibilidade | Funcionamento nos navegadores modernos (Chrome, Firefox, Edge e Safari). |
| **RNF05** | Usabilidade | Navegação clara e consistente entre as páginas, com microinterações (hover e foco) que orientam o usuário. |
| **RNF06** | Manutenibilidade | Separação de responsabilidades (separation of concerns): HTML, CSS e JavaScript em arquivos distintos, com CSS único reaproveitado pelas duas páginas (princípio DRY). |
| **RNF07** | SEO | Uso de title descritivo, meta description e marcação semântica para melhor indexação e compartilhamento. |

# **5\. Recursos da Página (Features)**

## **5.1 Cabeçalho e navegação**

Cabeçalho fixo (sticky header) presente nas duas páginas, com a logomarca à esquerda (clicável, retornando à home) e o menu de navegação à direita: Início, Serviços, Rastreamento e o botão de destaque “Fale Conosco”. A navegação utiliza âncoras internas e rolagem suave.

## **5.2 Seção principal (Hero)**

Bloco de abertura com fundo escuro de alto contraste, título com palavra de destaque em vermelho, texto de proposta de valor e dois botões de ação (CTA). Comunica imediatamente o propósito da empresa.

## **5.3 Nossas Soluções (cards)**

Três cartões responsivos (1 coluna no celular, 3 colunas no desktop) apresentando FCL, Consolidação LCL e Inspeção de Carga. Cada card possui ícone vetorial (SVG), descrição e link “Saiba mais” que direciona ao detalhamento na página de serviços. Os cards possuem microinteração de elevação ao passar o mouse (hover).

## **5.4 Rastreamento**

Campo de busca para o número do BL/Container com botão “Rastrear”. A interação é tratada em JavaScript: valida o preenchimento e exibe uma mensagem de retorno. Representa, no front-end, a futura integração com um serviço real de rastreamento.

## **5.5 Contato**

Seção dividida em duas colunas (empilhadas no celular): informações de contato (telefone, e-mail e endereço, com ícones) e um formulário com nome, e-mail, tipo de serviço e mensagem. O envio é tratado por JavaScript, com validação e mensagem de confirmação, sem recarregar a página.

## **5.6 Rodapé**

Rodapé compartilhado com identificação da empresa, ano e links institucionais (Termos de Uso e Política de Privacidade).

## **5.7 Página de Serviços**

Página com cabeçalho próprio (page header) e três blocos detalhados — FCL, LCL e Inspeção de Carga — cada um com ícone e descrição completa. Os blocos possuem âncoras que recebem o usuário vindo dos links “Saiba mais” da home, com deslocamento de rolagem ajustado (scroll-margin) para não ficar encoberto pelo cabeçalho fixo.

# **6\. Decisões de Layout e Interface**

## **6.1 Identidade visual e logomarca**

A identidade gira em torno da logomarca da Conex, em tons de azul. O azul-marinho foi adotado como cor institucional (confiança, seriedade logística) e o vermelho como cor de ação, criando contraste e guiando o usuário para os botões de conversão. A logomarca aparece no cabeçalho e, recortada em seu símbolo, como favicon.

## **6.2 Paleta de cores**

| Cor | Hex | Aplicação |
| :---- | :---- | :---- |
| Azul-marinho | \#1E3A8A | Cor institucional: logomarca, títulos de destaque e bordas. |
| Azul vivo | \#2563EB / \#1D4ED8 | Detalhes da marca e botão de rastreamento (incluindo hover). |
| Vermelho | \#DC2626 | Cor de ação (CTA): botões principais, links em hover e barras de destaque. |
| Vermelho escuro | \#B91C1C | Estado hover dos botões vermelhos. |
| Vermelho claro | \#EF4444 | Palavra de destaque no título do hero. |
| Grafite | \#111827 | Fundos escuros (hero e rodapé) para contraste. |
| Cinzas claros | \#F9FAFB / \#F3F4F6 | Fundo geral e de seções. |
| Branco | \#FFFFFF | Fundo do cabeçalho, cards e área de contato. |
| Tons de cinza | \#1F2937 … \#9CA3AF | Textos (corpo, secundário e dicas). |

## **6.3 Tipografia**

Optou-se por uma fonte sans-serif do sistema (system font), priorizando legibilidade e desempenho, sem o custo de carregar fontes externas (web fonts). A hierarquia é construída por tamanho e peso: títulos grandes e em negrito (font-weight 800\) no hero e nas seções, e corpo de texto com peso regular.

## **6.4 Estrutura de layout**

O conteúdo é centralizado em um contêiner com largura máxima de 1200px. O layout usa CSS Grid para os cards e o formulário, e Flexbox para o cabeçalho e a área de contato. A abordagem é mobile-first, com adaptações via media queries: os cards passam de 1 para 3 colunas (≥ 768px) e a área de contato passa de empilhada para duas colunas (≥ 1024px).

## **6.5 Experiência do usuário (UX)**

Foram aplicadas microinterações para tornar a navegação mais fluida e responsiva ao usuário:

•      Cabeçalho fixo (sticky), mantendo a navegação sempre acessível.

•      Rolagem suave (smooth scroll) ao navegar entre seções.

•      Elevação dos cards e mudança de cor de botões e links ao passar o mouse (hover).

•      Destaque visual no campo de formulário em foco (mudança da cor da borda).

# **7\. Tecnologias Aplicadas (Stack)**

## **7.1 Linguagens e técnicas**

| Tecnologia | Padrão | Uso no projeto |
| :---- | :---- | :---- |
| **HTML** | HTML5 | Estrutura semântica e conteúdo (header, section, nav, form, footer). |
| **CSS** | CSS3 | Estilização, layout (Flexbox e Grid), responsividade e transições. |
| **JavaScript** | ES6 (vanilla) | Interatividade: manipulação do DOM, eventos, validação e simulações. |
| **SVG** | — | Ícones vetoriais escaláveis, sem perda de qualidade. |
| **Git / GitHub** | — | Versionamento do código e hospedagem via GitHub Pages. |
| **VS Code** | — | Ambiente de desenvolvimento (editor de código). |

## **7.2 Justificativa da escolha**

Embora a disciplina permita o uso de frameworks (Bootstrap, React, Angular), o grupo optou por HTML, CSS e JavaScript puros (vanilla). A decisão se justifica pelo escopo do projeto — uma landing page institucional e estática — e pelos seguintes fatores:

•      Desempenho: ausência de bibliotecas e de etapa de build (bundler) resulta em páginas leves e de carregamento rápido.

•      Portabilidade: por gerar apenas arquivos estáticos, a aplicação roda em qualquer serviço de hospedagem, como o GitHub Pages.

•      Domínio dos fundamentos: o uso direto das tecnologias-base demonstra o entendimento de HTML, CSS e JavaScript, alinhado aos objetivos da disciplina.

•      Manutenção simples: menos dependências significam menos pontos de falha e atualização.

## **7.3 Estrutura de arquivos**

O projeto adota uma organização por responsabilidade, separando marcação, estilo, scripts e recursos:

Trabalho/  
├── index.html    	(página inicial)  
├── servicos.html 	(detalhamento dos serviços)  
├── css/  
│   └── style.css 	(estilos compartilhados)  
├── js/  
│   └── script.js 	(interações: rastreamento e formulário)  
└── assets/  
    ├── conex-logo.png (logomarca do cabeçalho)  
    └── favicon.png	(ícone da aba do navegador)

# **8\. Hospedagem (Deployment)**

A aplicação é publicada por meio do GitHub Pages, a partir de um repositório dedicado ao projeto. O código-fonte fica versionado no GitHub e a página é acessível por uma URL pública.

**Repositório:** \[https://github.com/Junior-dev01/Conex \]

**Página publicada:** \[https://junior-dev01.github.io/Conex/Conex/ \]

# **9\. Limitações e Trabalhos Futuros**

Por se tratar de uma entrega focada no front-end, alguns recursos são simulados e podem evoluir em versões futuras:

•      Rastreamento e formulário de contato são tratados apenas no cliente (client-side). Evolução: integração com uma API real de rastreamento e um back-end para envio de e-mails e armazenamento das solicitações.

•      O menu de navegação ainda não colapsa em um menu “hambúrguer” em telas muito pequenas. Evolução: implementar menu responsivo móvel.

•      As páginas de Termos de Uso e Política de Privacidade são links reservados (placeholder). Evolução: criar o conteúdo dessas páginas.

[image1]: <data:image/png;base64,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>