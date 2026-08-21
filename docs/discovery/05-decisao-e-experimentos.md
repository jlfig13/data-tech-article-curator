# 05 — Decisão e experimentos

## 5.1 As três perguntas de fechamento

**O problema é promissor, incerto ou fraco?**
→ **Fraco na forma como foi enunciado; incerto na forma reduzida.** Ver [doc 04](04-forca-do-problema.md).

**Qual é a maior incerteza restante?**

> ### O gargalo está na **coleta** ou no **consumo**?
>
> Se está na coleta, o sistema imaginado é a resposta certa.
> Se está no consumo, o sistema imaginado **não muda nada** — apenas produz uma pilha maior de
> conteúdo não lido, com melhor engenharia.
>
> Todo o resto (fontes, ranking, deduplicação, embeddings, UI de busca) é secundário e só faz
> sentido depois que essa pergunta tiver resposta.

**Qual é a menor evidência necessária para decidir?**
→ **E0 + E1 abaixo. Custo total: ~40 minutos hoje e 2 semanas de espera passiva. Zero linha de código.**

## 5.2 Escada de experimentos

Cada degrau só é escalado se o anterior passar. **Não pule degraus** — pular é como o projeto vira
três semanas de pipeline para um feed que ninguém abre.

---

### E0 — Auditoria retrospectiva `~40 min, hoje`

**Pergunta:** já existe conteúdo bom chegando até você e sendo ignorado?

**Como:** responder Q1, Q2, Q4 e Q8 do [doc 02](02-mom-test.md) **com fontes verificáveis** —
histórico do navegador (90 dias), busca por `unsubscribe` na caixa de entrada (60 dias), contagem de
abas/favoritos/itens salvos nunca lidos.

**Critério de falsificação:**
> Se houver **≥10 itens técnicos salvos e não lidos** ou **≥2 newsletters assinadas com baixa taxa
> de abertura**, o gargalo é **consumo**. A solução imaginada está descartada na forma atual.
> Vá direto para E2-alt.

---

### E1 — Teste de consumo com oferta pronta `2 semanas, custo ~0`

**Pergunta:** com conteúdo relevante chegando sem nenhum esforço seu, você lê?

**Como:** assinar 2 newsletters da área + ler o radar editorial mais recente
([doc 03](03-alternativas-atuais.md)). Sem construir nada. Registrar em uma nota simples: o que
chegou, o que foi aberto, o que foi terminado.

**Critério de sucesso:**
> Ler até o fim **≥50% dos itens** ao longo de 2 semanas.
> **Se falhar:** o problema não é coleta. Confirmado. **Pare.** Construir o coletor seria construir
> mais oferta para um gargalo de demanda.

---

### E2 — Concierge (Mágico de Oz) `2 semanas, manual`

*Só se E1 passar.*

**Pergunta:** curadoria **personalizada** produz resultado melhor que curadoria genérica — e o
suficiente para justificar automatizar?

**Como:** 30 min por semana, manualmente, escolher **5 itens** (sendo pelo menos 2 de tecnologias
que você ainda não conhece) e jogar num documento único. Nada de código, banco, pipeline ou UI.

**Critério de sucesso — e este é o único que importa de verdade:**
> **≥1 tecnologia nova entrou em avaliação prática** — você rodou um tutorial, subiu um contêiner,
> leu a documentação com intenção de usar. **Não** "achei interessante". **Não** "salvei para depois".
> Uma ação.
>
> Se 10 itens curados a dedo não produzem uma única ação em 2 semanas, nenhum volume de automação
> vai produzir.

---

### E2-alt — Atacar o consumo, não a coleta `2 semanas`

*Se E0 ou E1 falharem — este é o caminho provável.*

O problema real vira **hábito**, e a intervenção correta não é software:

- Um bloco fixo de 30 min na agenda, um dia por semana, com fonte já definida (sem escolher na hora
  — escolher é o que mata o hábito).
- Um compromisso social: 2–3 colegas, um item por semana, 15 min de conversa. Compromisso com outra
  pessoa é o mecanismo de adesão mais eficaz e o mais subestimado.
- Uma ferramenta de fila de leitura (Problema C), que é barata e resolve recuperação sem construir nada.

**Critério:** 4 semanas seguidas de bloco cumprido. Se o hábito não sustenta com fricção zero, ele
não vai sustentar com um produto próprio no meio.

---

### E3 — MVP mínimo `só depois de E2 passar`

**Escopo permitido — e nada além:**
- 5 a 10 fontes RSS/API fixas, escolhidas com base no que **de fato** foi lido em E1/E2.
- Um script agendado + um arquivo Markdown ou SQLite de saída.
- **Sem** classificador, **sem** embeddings, **sem** UI, **sem** buscador.

O buscador organizado, a deduplicação semântica e a descoberta adjacente só entram quando houver
volume acumulado suficiente para que a busca tenha o que buscar — e evidência de que o feed é lido.

## 5.3 Métrica que deve governar o projeto inteiro

Se algo for construído, a métrica **não** pode ser volume coletado, fontes cobertas ou precisão do
classificador. Todas essas são métricas de coleta, e coleta nunca foi o problema.

> **Métrica única: número de tecnologias novas que entraram em avaliação prática por mês.**
> **Meta inicial: 1 por mês.**

Um sistema que colete 10.000 artigos e produza zero avaliações práticas falhou. Um documento
manual com 5 links que produza uma avaliação por mês teve sucesso — e custou 30 minutos.

## 5.4 Próximo passo concreto

**Fazer o E0 hoje.** Responder Q1, Q2, Q4 e Q8 do [doc 02](02-mom-test.md) com fontes verificáveis,
registrar as respostas, e voltar aqui para decidir entre E1 e E2-alt.

Tempo estimado: 40 minutos. É a diferença entre construir a coisa certa e construir uma coisa bonita.
