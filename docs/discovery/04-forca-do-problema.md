# 04 — Força do problema

## 4.1 Pontuação (1 a 5)

Pontuação **provisória**, baseada apenas no que foi declarado. Ela não valida nem invalida nada —
serve para comparar este problema com outros e para explicitar onde a evidência falta.

| Critério | Nota | Justificativa |
|---|:---:|---|
| **Frequência** | 2 | O *desejo* de estar atualizado é permanente. O *evento de dor* (descobrir algo tarde e sentir consequência) apareceu **uma vez** em todo o enunciado: DuckDB. Um caso em anos é raridade, não recorrência. |
| **Impacto** | 2 | Nenhum custo concreto foi citado. Não houve projeto perdido, retrabalho, vaga perdida ou dinheiro gasto. O impacto relatado é desconforto, não prejuízo. Sobe para 4–5 se Q3 revelar um custo real. |
| **Esforço atual** | 1 | Praticamente nenhum. O próprio enunciado diz: "não tenho o hábito de acompanhar, pesquisar e ler". Não há gambiarra, planilha, script, alarme ou assinatura mantida. **Ausência de esforço é a evidência mais negativa deste quadro.** |
| **Insatisfação** | 4 | Alta — e genuína. Mas é insatisfação *declarada*, e declaração é a moeda mais barata do Discovery. |
| **Alternativas** | 2 | Existem muitas alternativas boas e gratuitas, e **nenhuma foi testada a fundo**. Nota baixa aqui significa "as alternativas resolvem razoavelmente bem" — não que sejam perfeitas, mas que a lacuna delas não foi demonstrada. |
| **Total** | **11/25** | |

## 4.2 O padrão que esse perfil revela

**Insatisfação alta (4) + esforço atual mínimo (1)** é a assinatura clássica de um problema do tipo
*"seria legal"*, não *"preciso resolver"*.

Quando um problema dói de verdade, as pessoas deixam rastro **antes** de existir uma solução boa:
improvisam, pagam por paliativos, montam planilha, criam rotina ruim mas própria. Aqui, o rastro é
ausente. O que existe é uma **intenção sincera** — que é uma coisa real e legítima, mas não é a
mesma coisa que uma dor.

## 4.3 Evidências

### Fortalecem o problema
- A área realmente se move rápido; a defasagem técnica tem custo de carreira real e conhecido.
- A insatisfação é específica e não genérica — há um caso nomeado (DuckDB), não só um mal-estar difuso.
- O interesse é durável: não é impulso de um dia, é um incômodo que persiste.
- O usuário tem capacidade técnica de construir a solução (custo de execução baixo).

### Enfraquecem o problema
- **Esforço atual zero.** Nada foi tentado e abandonado por limitação — simplesmente não foi tentado.
- **Um único caso concreto em anos**, e sem consequência mensurável.
- **Alternativas gratuitas e maduras não exploradas** (radar editorial, newsletters, RSS).
- **A dor declarada (não ler) e a solução proposta (coletar mais) não se encontram.**
- **Risco de solução que agrava o sintoma:** mais conteúdo agregado = mais dívida de leitura visível.
- **Viés de construtor:** a ideia é tecnicamente divertida (crawling, embeddings, ranking, busca
  semântica). Existe uma chance concreta de o desejo real ser *construir isso*, não *resolver isso* —
  o que é perfeitamente legítimo, mas muda completamente os critérios de sucesso do projeto.

## 4.4 Veredito provisório

> ### O problema é **FRACO a INCERTO**.
>
> Fraco na formulação atual ("preciso de um coletor"). Incerto na formulação reduzida
> ("quero um mecanismo que me faça, de fato, consumir e reter conhecimento técnico novo").
>
> **Não há evidência suficiente para justificar construir o sistema imaginado.** Há evidência
> suficiente para justificar **duas semanas de teste barato** antes de escrever a primeira linha
> de código.

## 4.5 Uma ressalva justa

Nada disso significa "não faça". Este é um projeto **pessoal**, com n=1 e custo de errar baixo. Se a
decisão for construir por prazer técnico e aprendizado, essa é uma decisão perfeitamente boa — só
precisa ser tomada **com esse nome**. O que o Discovery impede é a versão cara do erro: passar
semanas construindo pipeline, classificador e buscador, para descobrir depois que o feed não é
aberto — que é exatamente o destino já registrado nas newsletters não lidas da caixa de entrada.
