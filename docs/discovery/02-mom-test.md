# 02 — The Mom Test (auto-investigação)

Aqui há uma dificuldade honesta: **o usuário e o autor da ideia são a mesma pessoa.** Auto-entrevista
é o cenário mais fácil de enviesar que existe — você já sabe qual resposta salva a ideia.

Compensação: **não responder de memória.** Toda pergunta abaixo tem uma **fonte de verificação
externa** ao lado. Memória confirma a ideia; histórico de navegador não tem esse compromisso.

## 2.1 Perguntas sobre comportamento passado

Responda em `respostas.md` (não versionado por padrão) ou direto neste arquivo.

| # | Pergunta | Onde verificar (não responder de cabeça) |
|---|---|---|
| Q1 | Nos últimos 30 dias, quais artigos técnicos você **terminou** de ler? Liste título e onde achou. | Histórico do navegador, "lidos depois", Pocket/Readwise |
| Q2 | Quantas newsletters técnicas você assina hoje? Das últimas 10 edições recebidas, quantas você **abriu**? | Caixa de entrada — busque por `unsubscribe` nos últimos 60 dias |
| Q3 | No caso DuckDB: qual foi a **consequência concreta** de ter descoberto tarde? Perdeu vaga, refez um pipeline, gastou dinheiro em algo desnecessário, passou vergonha numa reunião? Ou apenas "poxa, seria legal ter sabido antes"? | Memória + histórico de projetos daquele período |
| Q4 | Quantos links técnicos estão salvos/abertos agora e nunca foram lidos? | Abas abertas, favoritos, itens salvos no LinkedIn, mensagens salvas no Slack/WhatsApp |
| Q5 | Qual foi a **última vez** que você precisou avaliar uma tecnologia nova para uma decisão real? O que fez para decidir? | Histórico de projetos, PRs, docs de arquitetura |
| Q6 | Quantas vezes nos últimos 6 meses alguém citou uma tecnologia da sua área que você não conhecia? Cite os casos. | Memória, mas com nomes — se não lembra de nenhum caso além do DuckDB, isso é um dado |
| Q7 | O que você **já tentou** para resolver isso? (Feedly, newsletter, meta de leitura, curso, lista de estudo) Por quanto tempo durou e por que parou? | Contas criadas, apps instalados e abandonados |
| Q8 | Quanto tempo por semana você **de fato** gastou lendo conteúdo técnico no último mês? | Tempo de tela / histórico. Não estime — meça |
| Q9 | Você já **pagou** por algo relacionado (curso, assinatura, livro, conferência)? Usou? | Extrato/cartão dos últimos 12 meses |
| Q10 | Quando você descobriu o DuckDB, **como** descobriu? | Reconstruir a cadeia — ela indica qual canal já funciona para você |

## 2.2 Perguntas proibidas neste Discovery

Não faça, nem a si mesmo:

- ~~"Você usaria um radar automático de tecnologia?"~~
- ~~"Seria útil receber isso toda semana?"~~
- ~~"A ideia é boa?"~~
- ~~"Você gostaria de descobrir tecnologias antes dos outros?"~~

Todas têm resposta "sim" garantida e valor informativo zero.

## 2.3 Como interpretar as respostas

**Sinal forte (o problema existe e é de coleta):**
- Q1 lista ≥4 artigos terminados, vindos de fontes espalhadas e caçados manualmente.
- Q4 é baixo (você lê o que salva).
- Q3 tem um custo concreto e nomeável.
- Q7 mostra tentativas sustentadas que esbarraram numa limitação específica da ferramenta.

**Sinal fraco (o problema é de consumo, ou é preferência):**
- Q1 lista 0–1 artigos.
- Q2 mostra newsletters assinadas e não abertas → *conteúdo já chega e não é lido*.
- Q4 é alto → *já existe um estoque de conteúdo bom parado*.
- Q3 não tem custo, só desconforto.
- Q7 mostra tentativas que morreram em dias, sem limitação técnica identificável.

> **A combinação Q2 alto + Q4 alto + Q1 baixo é fatal para a solução imaginada.** Significa que a
> oferta de conteúdo relevante já excede a capacidade de consumo. Nesse cenário, aumentar a oferta
> (que é exatamente o que um crawler faz) piora o problema em vez de resolvê-lo.
