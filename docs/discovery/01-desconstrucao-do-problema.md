# 01 — Desconstrução do problema

## 1.1 Pressupostos embutidos na ideia

Cada linha abaixo é algo tratado como verdade no enunciado original, mas que **ainda não foi
demonstrado**. Um pressuposto falso aqui derruba a solução inteira.

| # | Pressuposto | Por que é frágil | Como falsificar |
|---|---|---|---|
| P1 | "O gargalo é a coleta de conteúdo" | O texto diz que falta *hábito de ler*, não que falta conteúdo. Conteúdo bom já é abundante e gratuito. | E0/E1 (doc 05) |
| P2 | "Se o conteúdo chegar pronto, eu vou ler" | Newsletter não lida e aba salva e nunca aberta são o contraexemplo mais comum do mundo. | E1 |
| P3 | "Descobrir tarde causa prejuízo" | Nenhum custo concreto foi citado no caso DuckDB — nem projeto perdido, nem retrabalho, nem vaga. | Q3 (doc 02) |
| P4 | "A necessidade é contínua" | Pode ser episódica: aperta quando há uma decisão técnica, uma entrevista ou uma conversa — não todo dia. | Q5, Q6 (doc 02) |
| P5 | "As alternativas existentes não servem" | Nenhuma foi usada de forma sustentada. Não usar ≠ não servir. | Doc 03 |
| P6 | "Automação cria hábito" | Automação remove esforço de *coleta*. Hábito depende de gatilho, contexto e recompensa — nada disso é resolvido por um crawler. | E2 |
| P7 | "Preciso descobrir coisas que ainda não conheço" | Descoberta serendipitosa é o requisito mais caro do sistema (é o que exige embeddings/ranking/expansão semântica) e o menos evidenciado como dor real. | E2 |
| P8 | "O problema é meu como usuário único" | n=1. Não há validação externa. Não é fatal para uso pessoal, mas impede qualquer generalização. | — |

**O pressuposto de maior alavancagem é o P1.** Se ele cair, o produto imaginado é o produto errado,
por melhor que seja construído.

## 1.2 Reformulação neutra do problema

A formulação original já contém a solução ("quero criar um radar... que busque conteúdos"). Versão
neutra, sem embutir resposta:

> **Um profissional de dados quer manter sua leitura de mercado atualizada ao longo dos anos, mas
> não sustenta nenhuma rotina de acompanhamento técnico. O sintoma percebido é tomar conhecimento
> de tecnologias relevantes depois de seus pares. O custo real desse atraso ainda não foi
> mensurado.**

Três problemas *distintos* estão colapsados em um só no enunciado original:

- **Problema A — Cobertura:** "não sei o que existe lá fora." (problema de coleta)
- **Problema B — Consumo:** "não leio o que já poderia estar lendo." (problema de hábito/atenção)
- **Problema C — Recuperação:** "li algo há 6 meses e não acho mais." (problema de busca/memória)

A solução imaginada ataca **A** (e um pouco de C). A dor declarada é **B**. Definir qual deles
merece ser resolvido é o objetivo do diamante "Definir".

## 1.3 Jobs To Be Done

### Job funcional
> Quando **alguém menciona uma tecnologia da minha área que eu não conheço** — em uma reunião de
> arquitetura, numa vaga, num post — quero **já ter ouvido falar dela e ter uma noção do que
> resolve**, para **conseguir participar da decisão e não descobrir a coisa tarde demais**.

Note o formato: o job dispara em **um evento**, não em "todo dia às 8h". Isso é central.

### Job emocional
Reduzir a ansiedade de estar defasado. "Estar em dia" é, em parte, uma necessidade de
**reasseguramento**, não de informação. Um radar que entrega 40 itens por semana pode *aumentar*
essa ansiedade em vez de reduzi-la — a pilha de não lidos vira uma dívida visível.

### Job social
Ser percebido (no time, em entrevistas, no LinkedIn) como alguém que acompanha a evolução da área.

### Contexto e gatilhos
| Gatilho | Frequência estimada | Natureza |
|---|---|---|
| Decisão de arquitetura ("qual engine/orquestrador?") | poucas vezes por ano | **pull** — busca ativa no momento |
| Entrevista ou movimentação de carreira | eventual | **pull** |
| Colega/comunidade menciona algo desconhecido | semanal? | **push** — surpresa |
| Tempo livre com intenção de estudar | ? | ambíguo |

**Consequência incômoda:** se os gatilhos de maior impacto são *pull* (nascem de uma pergunta
específica), a resposta certa pode ser **melhorar a pesquisa no momento da necessidade** — algo que
uma boa busca com LLM já faz hoje, sem construir nada — e não manter um radar contínuo rodando.

### Como resolve hoje
Essencialmente: **não resolve**. Absorve por osmose (colegas, LinkedIn, algoritmo) e pesquisa sob
demanda quando o assunto aparece. Custo atual ≈ zero.

> **Atenção:** "custo atual ≈ zero" é uma evidência que **enfraquece** o problema, não que o
> fortalece. Problemas fortes deixam rastro de esforço — gambiarras, planilhas, alarmes, dinheiro
> gasto. Aqui não há rastro. Ver doc 04.
