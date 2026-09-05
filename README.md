# 🤖 Automação com IA em Python

## ✨ Contexto e Objetivos:

### ✨ Contexto

O avanço da Inteligência Artificial abriu novas possibilidades para a automação de tarefas cotidianas e fluxos de trabalho complexos. A combinação da IA com a linguagem Python — conhecida por sua simplicidade, vasta biblioteca de ferramentas e forte presença na comunidade de dados — permite criar soluções inteligentes capazes de ler, interpretar e agir sobre informações de forma autônoma. Este caderno temático explora a integração dessas tecnologias para resolver problemas reais de forma eficiente.

### ✨ Objetivos

- Compreender fundamentos: Entender como utilizar Python para criar scripts de automação de tarefas rotineiras.
- Integrar Inteligência Artificial: Aprender a conectar e consumir APIs de IA (como modelos de linguagem) dentro de aplicações Python.
- Desenvolver fluxos inteligentes: Criar automações que não apenas sigam regras rígidas, mas que consigam tomar decisões simples e processar dados não estruturados.
- Criar um material de consulta: Consolidar os aprendizados, referências, prompts e códigos úteis para servirem como base de conhecimento para projetos futuros.


## 🚀Curadoria de Fontes:

### 1️⃣ Vídeos:

https://www.youtube.com/watch?v=f9exUjUONGI
https://www.youtube.com/watch?v=uEoqY3eavhk
https://www.youtube.com/watch?v=MeOUl7ZjJRM&vl=pt-BR

### 2️⃣ PDF:

- apostila/Apostila Jornada Python - Aula 1.pdf
- apostila/Apostila Jornada Python - Aula 2.pdf
- apostila/Apostila Jornada Python - Aula 3.pdf
- apostila/Apostila Jornada Python - Aula 4.pdf


## 🎯Engenharia de Prompts e "Cicatrizes":

Neste projeto, o principal objetivo foi desenvolver um bot em Python para automatizar jogadas no MMORPG **OGame** (disponível em [Lobby OGame](https://lobby.ogame.gameforge.com/pt_BR/hub)). O foco central da automação foi otimizar e executar as **missões de exploração** (expedições).

### 🚧 Desafios e "Cicatrizes"
O maior desafio técnico encontrado durante a criação deste bot foi o mapeamento de interface: **capturar com precisão as coordenadas X e Y na tela para todos os planetas do jogo**.

Como a interface de jogos de navegador pode ser dinâmica, possuir animações e variar de acordo com a resolução da tela, garantir que o bot clicasse no lugar exato de forma repetitiva e confiável exigiu muita pesquisa e teste.

**Como a IA auxiliou no Troubleshooting:**
- **Abordagens Dinâmicas:** Utilizei a IA para explorar alternativas às coordenadas fixas (hardcoded). Pedi sugestões de como usar bibliotecas como `pyautogui` com `locateOnScreen` ou `OpenCV` para encontrar os planetas baseando-se em imagens/padrões, tornando o bot muito mais resiliente.
- **Lógica de Verificação:** Usei prompts para implementar lógicas de espera (waits), evitando que o script rodasse mais rápido do que o jogo carregava a tela.

### 💡 Exemplo de Prompt Utilizado
> *"Estou criando um bot em Python para automatizar missões no OGame usando pyautogui. O maior problema é pegar o ponto X e Y da tela de todas as coordenadas dos planetas do jogo de forma confiável. Como posso fazer o script identificar esses planetas de forma dinâmica, sem depender de posições absolutas que podem quebrar se a janela mudar de tamanho?"*


## 🧩 Miniguia de Estudo (Entrega Final)

### 1️⃣ Resumo Estruturado: Automação com IA em Python
A integração de IA com Python transforma scripts tradicionais em ferramentas cognitivas. O fluxo de desenvolvimento geralmente envolve:
- **Coleta e Preparação:** Usar bibliotecas Python (como `pandas`, `requests`, `BeautifulSoup`) para extrair e limpar dados.
- **Processamento com IA:** Enviar dados para APIs de modelos de linguagem (como OpenAI, Gemini, Anthropic) para classificação, tradução, extração de entidades ou tomada de decisão.
- **Ação:** Utilizar a resposta da IA para executar tarefas subsequentes, como enviar e-mails, atualizar bancos de dados, ou acionar webhooks em ferramentas como o n8n.

### 2️⃣ Glossário de Conceitos
- **API (Application Programming Interface):** A ponte que permite que seu código Python se conecte e converse com serviços externos de IA.
- **LLM (Large Language Model):** Modelo de Inteligência Artificial treinado em grandes volumes de texto, capaz de compreender e gerar linguagem natural.
- **Prompt Engineering:** A técnica de elaborar, refinar e otimizar instruções para extrair o melhor resultado possível de uma IA.
- **Token:** A unidade básica (pedaço de palavra) que a IA utiliza para processar textos. O consumo das APIs é geralmente calculado por tokens.
- **Webhooks:** Mecanismo que permite que sistemas diferentes se comuniquem em tempo real através de eventos (muito usado em integrações com o n8n).

### 3️⃣ Prompts Reutilizáveis
Aqui estão alguns "prompts coringas" para ajudar na criação e manutenção de automações:

- **Para criar scripts base:** 
  > "Atue como um Engenheiro de Dados Sênior. Escreva um script em Python que se conecte na API do [SERVIÇO] para realizar a [TAREFA]. Por favor, inclua tratamento de erros estruturado (try/except), utilize variáveis de ambiente (.env) para chaves sensíveis e comente o código detalhadamente."

- **Para debugar e corrigir erros (Troubleshooting):**
  > "Estou rodando uma automação em Python e recebendo o seguinte erro: `[COLE O ERRO AQUI]`. O trecho de código responsável é este: `[COLE O CÓDIGO]`. Analise o problema passo a passo e me mostre a correção recomendada."

- **Para estruturação de dados (Data Parsing):**
  > "Vou te passar um bloco de texto não estruturado. Preciso que você analise o conteúdo e me devolva APENAS um objeto JSON válido, contendo as chaves: `['nome', 'data', 'valor']`. Texto: `[COLE O TEXTO]`."
