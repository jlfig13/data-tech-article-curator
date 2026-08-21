# 03 — Alternativas atuais

A existência de alternativas não invalida o problema. O que importa é: **quais foram realmente
tentadas, por quanto tempo, e onde exatamente falharam.** Uma alternativa nunca tentada não é
evidência de que ela não serve — é evidência de que o problema não doeu o bastante para procurar.

*(Nomes abaixo são pontos de partida; confirme disponibilidade e formato atual antes de assinar.)*

## 3.1 Mapa das alternativas

| Categoria | Exemplos | Cobre qual problema | Custo de entrada | Já tentado? |
|---|---|---|---|---|
| **Radares editoriais** | Thoughtworks Technology Radar, InfoQ Trends Reports, relatórios de tendências de fornecedores | A (cobertura) — é literalmente a solução imaginada, feita por um time editorial | Grátis, ~1h a cada 6 meses | ⬜ |
| **Newsletters de nicho em dados** | Data Engineering Weekly, Blef.fr Data News, SeattleDataGuy, boletins "TLDR"-style | A + curadoria já filtrada | Grátis, 10 min/semana | ⬜ |
| **Agregadores/RSS** | Feedly, Inoreader, RSS via app de leitura | A, com controle de fontes | Grátis–baixo, ~1h de setup | ⬜ |
| **Comunidades** | Hacker News, Lobsters, r/dataengineering, Discords/Slacks da área | A + serendipidade (o ponto forte real deles) | Grátis, hábito | ⬜ |
| **Sinal de adoção** | GitHub Trending, star history, releases de projetos, Stack Overflow Survey | A, com sinal de *tração* e não só de buzz | Grátis | ⬜ |
| **Leitura com fila e memória** | Readwise Reader, Pocket, Instapaper, Obsidian + clipper | **B (consumo) e C (recuperação)** | Grátis–pago | ⬜ |
| **Busca sob demanda com LLM** | Deep research / busca conversacional no momento da dúvida | Atende os gatilhos *pull* sem manter nada rodando | Grátis–assinatura já existente | ⬜ |
| **Ritmo social** | Conferências, meetups, um grupo de leitura com 2–3 colegas | B — compromisso com outra pessoa é o mecanismo de hábito mais eficaz e o mais ignorado | Baixo | ⬜ |

## 3.2 O teste mais barato de todos

**O Thoughtworks Technology Radar é, essencialmente, a versão pronta e curada por especialistas da
ideia deste repositório.** Sai duas vezes por ano, é gratuito, e classifica tecnologias em
adotar/experimentar/avaliar/evitar — exatamente o recorte "o que está surgindo na minha área".

Pergunta desconfortável: **por que ele ainda não foi lido?**

- Se a resposta é "não conhecia": o problema não é falta de ferramenta, é falta de *procura*. Isso
  enfraquece muito a tese de que existe uma dor ativa.
- Se a resposta é "conheço, mas não leio": o gargalo é **consumo**, e nenhum crawler resolve isso.
- Se a resposta é "li e não serviu porque [motivo específico]": **aí sim** existe um requisito real e
  o Discovery tem material para trabalhar. Registre o motivo — ele vale mais que o resto do documento.

## 3.3 O que a solução imaginada faria melhor que tudo acima

Sendo rigoroso, resta pouco, e vale nomear com precisão:

1. **Personalização ao contexto específico** (stack que você usa, nível, idioma) — nenhuma
   alternativa faz isso.
2. **Recuperação (Problema C)** — busca sobre o que *você* já viu, ao longo de anos.
3. **Descoberta adjacente** — sugerir o vizinho do que você conhece, não o mais popular.

Esses três pontos são a única justificativa defensável para construir algo. **E os três dependem de
que o problema B (consumo) esteja resolvido primeiro** — personalizar e indexar conteúdo que não
será lido não produz valor nenhum.
