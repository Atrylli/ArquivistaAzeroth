# 📜 Arquivista do Gazeta de Azeroth – Caderno Temático NotebookLM

Repositório desenvolvido para o desafio da DIO, aplicando conceitos de engenharia de prompts, curadoria de fontes e inteligência artificial generativa baseada em RAG (Retrieval-Augmented Generation) através do **Google NotebookLM**.

---

## 🎯 1. Contexto e Objetivos

* **Objetivo do Projeto:** Este repositório sustenta um MVP (*Minimum Viable Product*) estruturado para validar a criação de um novo canal no YouTube voltado ao universo de *World of Warcraft*.
* **Assunto de Escopo Inicial:** Nesta versão focada e enxuta do MVP, a base de conhecimento e a curadoria de dados foram deliberadamente restritas a um único arco histórico central: *a trágica trajetória de Arthas Menethil (de príncipe herdeiro de Lordaeron a Lich King)*.
* **Objetivo do Estudo:** Validar a eficácia do Google NotebookLM como motor de RAG para atuar como um "Arquivista" especialista. A ferramenta foi projetada para transformar dados brutos de lore em roteiros jornalísticos e narrativas no estilo medieval, garantindo rigor cronológico absoluto, restrição estrita às fontes fornecidas e prevenção contra spoilers temporais para apoiar diretamente a produção de conteúdo do canal *Gazeta de Azeroth*.
---

## 📚 2. Curadoria de Fontes

Para alimentar a base de conhecimento do NotebookLM, foram selecionadas fontes oficiais e estruturadas:
1. **Wowpedia (Artigo Principal):** Biografia detalhada de Arthas Menethil.
2. **Imagens Conceituais e Visuais (`1.png`, `2.png`, `3.png`):** Elementos gráficos e de identidade visual criados para a página *Gazeta de Azeroth*.
3. **Literatura e Registros Oficiais:** Trechos de *Crônicas: Arthas, Rise of the Lich King* e relatórios de campanhas de Nortúndria.
4. **PDF:** Arquivo curto com o resumo cronológico da história do personagem *Arthas Menethil*.

<img width="447" height="504" alt="image" src="https://github.com/user-attachments/assets/af319d50-ea7c-4aa7-ae2b-6b18cdc39262" />

---

## ⚙️ 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Documentação do processo iterativo de refinamento do comportamento da IA:

* **Desafio Inicial:** Nas primeiras iterações, a IA tendia a misturar eventos futuros (como a queda do Rei Lich no *Wrath of the Lich King*) em momentos iniciais da narrativa de Lordaeron.
* **Correção / Cicatriz:** Ajustamos o prompt impondo uma trava temporal restritiva ("*Nunca faça spoilers de acontecimentos posteriores ao período retratado*") e definindo o tom narrativo estrito de um correspondente medieval contemporâneo aos fatos.
* **Prompt Estratégico Final Utilizado:**
  > *"Utilizando exclusivamente as fontes presentes neste Notebook, produza uma nova edição da Gazeta de Azeroth sobre a história [Escolho um momento da história do Arthas]. Escreva como um correspondente medieval que está registrando os acontecimentos para os Arquivos Centrais de Azeroth. A resposta deve conter: Manchete, Subtítulo, Corpo da matéria (no máximo palavras), Linha do tempo, Perfil do personagem, Notícias secundárias, Legenda de imagem, Curiosidade e Fontes. Nunca utilize informações externas e nunca faça spoilers."*

**Com isso, só preciso alterar o momento da história e ele gera um resumo estruturado para o jornal.**

Exemplo de resposta do NotebookLM:

<img width="731" height="488" alt="image" src="https://github.com/user-attachments/assets/de53cd91-2661-4135-bf45-67e74a442077" />

---

## 📖 4. Miniguia de Estudo (Entrega Final Consolidada)

### Resumo Estruturado do Assunto
* **A Ascensão:** A criação de Arthas sob a tutela da Aliança, seu treinamento com Muradin, sua consagração como Paladino do Punho de Prata por Uther e seu relacionamento com Jaina Proudmoore.
* **A Ruptura:** A disseminação da Praga da Morte-Viva por Kel'Thuzad, culminando no traumático *Expurgo de Stratholme* e no corte de laços com seus mentores.
* **A Queda:** A jornada obsessiva a Nortúndria, a destruição dos próprios navios, a aquisição da lâmina rúnica amaldiçoada *Frostmourne* e a perda de sua alma.
* **A Coroa:** O parricídio do Rei Terenas em Lordaeron, a destruição de Quel'Thalas e Dalaran, e a fusão final com o espírito de Ner'zhul no topo da Geleira Coroa de Gelo.

### Glossário de Conceitos
* **Praga da Morte-Viva:** Doença necromântica disseminada pelo Culto dos Malditos através de grãos contaminados para transformar civis em mortos-vivos.
* **Ordem do Punho de Prata:** Ordem sagrada de paladinos fundada para combater a Horda e, posteriormente, servir como bastião contra o Flagelo.
* **Frostmourne:** Lâmina rúnica malevolente forjada pelo Kil'jaeden, capaz de roubar a alma daquele que a empunha.
* **Flagelo (Scourge):** O exército de mortos-vivos comandado pelo Lich King.

### Prompts Reutilizáveis para Futuras Revisões
1. *Análise de Facções:* "Explique a dinâmica política entre o Kirin Tor e a Aliança de Lordaeron com base exclusivamente nas fontes deste caderno, estruturando a resposta em formato de memorando diplomático."
2. *Linha do Tempo Crítica:* "Gere uma linha do tempo estritamente cronológica dos eventos que antecederam a Terceira Guerra, apontando causas e consequências diretas para o reino de Quel'Thalas."
