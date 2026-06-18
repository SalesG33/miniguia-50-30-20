# 📘 Miniguia de Estudos: Orçamento Pessoal com a Regra 50/30/20 e NotebookLM

https://notebooklm.google.com/notebook/1793629c-e6f8-4691-b753-249f348ec391

Projeto prático desenvolvido para o desafio de projeto da DIO, com o objetivo de estruturar um guia de educação financeira pessoal utilizando inteligência artificial para curadoria e organização de fontes confiáveis.

---

## 🎯 Contexto e Objetivos
Escolhi o tema de Orçamento Pessoal, com foco na regra 50/30/20, pois achei interessante criar um guia prático que explique uma forma simples e consistente de economizar dinheiro. É um material pensado para ajudar pessoas que têm dificuldade com organização financeira (como eu). 

Meu objetivo com este projeto é explorar a capacidade do NotebookLM de sintetizar materiais complexos, cumprindo o desafio prático e, ao mesmo tempo, criando uma ferramenta real que eu possa utilizar no meu próprio dia a dia para melhorar minhas finanças.

---

## 📚 Curadoria de Fontes
As fontes oficiais utilizadas para alimentar a base de conhecimento da IA foram:
1. **Série Finanças Pessoais: Orçamento Pessoal** - Banco Central do Brasil (PDF)
2. **Método 50/30/20** - Vivest (PDF)
3. **Curso Educação Financeira Pessoal (Módulo 2: Planejamento)** - Escola de Governo do Distrito Federal (PDF)
4. **Cartilha de Planejamento Financeiro Familiar** - Caixa Econômica Federal (PDF)

---

## 🛠️ Engenharia de Prompts e "Cicatrizes"
Durante o desenvolvimento, explorei diferentes níveis de interação com a IA:
1. **Perguntas Sugeridas (NotebookLM):** Comecei testando as perguntas que a própria ferramenta gera ao ler os PDFs. As respostas foram satisfatórias e serviram para validar que os documentos foram lidos corretamente.
2. **Perguntas Estruturadas (Glossário e Ações):** Criei prompts específicos pedindo para a IA criar resumos didáticos e extrair lições práticas de economia doméstica.
3. **Criação de Comando Mestre (/raiox):** A maior "cicatriz" e aprendizado foi desenvolver um prompt que funciona como um comando de atalho. Precisei ajustar a instrução para que a IA entendesse que deveria fazer cálculos matemáticos simulados (tempo de recuperação com base nos 20% de poupança da regra) de forma rápida e direta.

---

## 📘 Miniguia de Estudo (Entrega Final)

### 1. Resumos Estruturados do Assunto
Com base nas fontes, o planejamento financeiro eficiente não depende de matemática complexa, mas sim de hábitos comportamentais. O primeiro passo é o **Raio-X Financeiro** (mapear ganhos e despesas). A ánalise dos dados ajuda a aplicar a **Regra 50/30/20** para dividir a renda líquida em três caixas:
*   **50% (Essenciais):** Gastos de sobrevivência (moradia, saúde, alimentação).
*   **30% (Estilo de Vida):** Gastos variáveis e desejos (lazer, jantares fora, assinaturas).
*   **20% (Prioridades Financeiras):** O foco principal para pagar dívidas e encher a Reserva de Emergência.

### 2. Glossário de Conceitos Aprendidos
*   **Orçamento Doméstico:** Tipo de planejamento que detalha receitas e despesas previstas. Funciona como um mapa de navegação das finanças.
*   **Despesas Fixas:** Contas pagas todos os meses com valores iguais ou muito parecidos (ex: aluguel, mensalidade escolar).
*   **Despesas Variáveis:** Gastos que mudam constantemente por preço ou consumo (ex: energia, telefone, mercado).
*   **Reserva de Emergência:** O "tanque de combustível" financeiro que deve ser mantido cheio para imprevistos (ex: remédios, consertos).
*   **Regra 50/30/20:** Regra de bolso que divide o orçamento em 50% para necessidades, 30% para desejos e 20% para poupança/investimentos.
*   **Comando `/raiox`:** Atalho personalizado de prompt criado para simular decisões de compra rápidas. Ele recebe três informações do usuário (sua renda líquida, o valor do que quer comprar e quanto tem guardado) e calcula instantaneamente a porcentagem consumida da reserva de emergência, a classificação do gasto e o tempo em meses para repor esse dinheiro.
    *   *Exemplo de uso:* `/raiox Renda: 3000, Compra: 1500, Reserva: 5000`

### 3. Prompts Reutilizáveis para Revisão e Rotina

#### A) Classificador de Gastos (50/30/20)
> *"Atue como meu assistente financeiro pessoal. Acabei de realizar o gasto: [NOME DA DESPESA OU PRODUTO] no valor de [VALOR]. Com base na regra 50/30/20, classifique este item em uma das três categorias (50% Essencial, 30% Estilo de Vida ou 20% Prioridade Financeira) e justifique brevemente. Se o gasto for variável, sugira uma forma de monitorá-lo para não estourar a categoria."*

#### B) Plano de Emergência (Corte de Gastos)
> *"Minha categoria de 30% (Estilo de Vida) estourou este mês. Com base nas lições de economia doméstica, sugira 5 ações imediatas para reduzir meus gastos variáveis sem sacrificar totalmente meu bem-estar, focando em redução de desperdício em contas de consumo e alternativas de lazer gratuitas."*

#### C) Comando Mestre: /raiox Financeiro (Configuração)
> *"A partir de agora, toda vez que eu digitar o comando /raiox, você deve atuar como meu analista financeiro especializado na Regra 50/30/20. Sua missão é realizar um Raio-X Financeiro imediato sobre uma intenção de compra. 
> Para o comando funcionar, eu fornecerei três dados: Renda Líquida Mensal, Valor Total da Compra e quanto tenho na Reserva de Emergência. 
> Responda obrigatoriamente calculando: 1) O comprometimento em % da reserva atual; 2) Classificação na regra 50/30/20; 3) Tempo de recuperação (meses necessários para repor o valor usando 20% da renda mensal); e 4) Veredito final (Prudente ou Perigoso)."*
