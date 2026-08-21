# 06 — Resultado do E0 (auditoria retrospectiva)

Respondido em 2026-08-21, de memória (sem checagem de histórico/inbox — registrado como
limitação, não escondido). Ver [02](02-mom-test.md) para as perguntas originais.

## 6.1 Respostas brutas

> **Q1 — O que você terminou de ler nos últimos 30 dias?**
> "Li sobre Supabase, Airflow, atualizações do Power BI, MCP Automate, Power Apps, atualização
> sobre Power Apps. Não tenho muito costume de ler, mas não quer dizer que não leio. Leio bastante
> notícia do mundo, mas artigos e notícias sobre tecnologia na minha área não acho em jornais. Não
> sei as fontes."

> **Q2 — Quantas newsletters assina, quantas abriu das últimas 10?**
> "Nenhuma. Vejo quando me deparo com problema real e procuro soluções, aprofundo o conhecimento
> antes de aplicar."

> **Q4 (na ordem em que foi respondida, referente a "links salvos e não lidos")**
> "Nenhum, mesmo problema: busco em IAs, vídeos e alguns artigos isolados na internet."

> **Q3 — Qual foi a consequência concreta de descobrir DuckDB tarde?**
> "Apliquei em um caso real de DataLake, entendi sobre tabelas colunares."

## 6.2 O que isso muda — e o que não muda

### A hipótese principal do E0 **não se confirmou, mas também não foi descartada da forma prevista**

O critério de corte registrado no [doc 05](05-decisao-e-experimentos.md#e0) era: *"se houver ≥10
itens salvos não lidos ou newsletters assinadas com baixa abertura, o gargalo é consumo."*
Isso não apareceu. **Não existe estoque de conteúdo represado.** Zero newsletters, zero links
salvos parados. Isso descarta o cenário que eu tinha como mais provável (P1 do
[doc 01](01-desconstrucao-do-problema.md): "content chega e não é lido").

Isso é importante o suficiente para dizer sem rodeios: **minha hipótese inicial estava errada.**
O padrão real é outro.

### O padrão real: 100% *pull*, 0% *push*

Você não tem — e nunca teve — nenhum canal de exposição passiva a tecnologia. Toda a sua leitura
técnica nasce de um problema real já em mãos: encontra o problema → pesquisa (IA, vídeos, artigos
isolados) → aprofunda → aplica. A lista de itens lidos no último mês (Supabase, Airflow, Power BI,
MCP, Power Apps) não é pequena — é **só que toda ela foi motivada por necessidade**, não por
descoberta ambiente.

Isso confirma com evidência real algo que no [doc 01](01-desconstrucao-do-problema.md) era só
hipótese (seção 1.3, "gatilhos"): **seus gatilhos são majoritariamente *pull*.** E dá um dado novo,
que muda o resto da análise.

### O dado novo, e o mais importante da rodada: "não sei as fontes"

Essa frase é diferente das outras. Não é sobre hábito — é sobre **capacidade**. Você não disse "não
tenho tempo de ler fontes de tecnologia"; disse que não sabe quais são. Isso reabre parcialmente o
Problema A (cobertura/descoberta), que no doc 04 eu tinha dado como fraco.

Mas — e isto precisa ser dito para não repetir o mesmo erro de antes — **essa frase ainda não foi
testada.** Existe uma diferença grande entre:

- (a) "eu já procurei fontes boas de tecnologia de dados e não encontrei nada que prestasse", e
- (b) "eu nunca cheguei a procurar, porque nunca precisei — só entro em modo de busca quando o
  problema já está em cima de mim."

A resposta a Q2 ("vejo quando me deparo com problema real") sugere fortemente que é **(b)**. Isso
não invalida o "não sei as fontes" — só significa que ele é uma lacuna de **exposição**, não de
**busca de fontes já tentada e frustrada**. É uma diferença crucial porque (a) exigiria construir
algo melhor que o que existe; (b) só exige *te apresentar* o que já existe.

### Um sinal muito bom, escondido na resposta 4

"Apliquei em um caso real de DataLake, entendi sobre tabelas colunares" é a melhor notícia deste
documento inteiro. Isso mostra que, no seu caso, **aprendizado gerado por necessidade real converte
em aplicação real** — não fica em "achei interessante", vira uso. Isso importa muito para o
[E2 (concierge)](05-decisao-e-experimentos.md#e2--concierge-mágico-de-oz-2-semanas-manual):
seu critério de sucesso ali era justamente "≥1 tecnologia nova entrou em avaliação prática". O seu
histórico dá razão para achar que isso é plausível — **se** o material chegar até você.

A pergunta em aberto não é mais "você converte aprendizado em ação" (parece que sim). É:
**"algo que chega sem que você tenha ido atrás vai, de fato, ser aberto e lido?"** — isso nunca foi
testado, porque você nunca experimentou receber nada assim.

## 6.3 Reformulação do problema (2ª versão)

A versão do doc 01 ainda estava contaminada pela hipótese errada (estoque represado). Nova versão,
baseada no E0:

> **Você tem um modo de aprendizado reativo e eficaz (pesquisa profunda quando um problema real
> aparece, e o que aprende costuma virar aplicação real) — mas nenhum canal de exposição passiva a
> tecnologias fora do seu radar imediato. Como resultado, você só descobre o que já sabe que
> precisa procurar. Tecnologias que resolveriam um problema que você nem sabe nomear (o caso
> DuckDB) ficam invisíveis até alguém ou algo mencioná-las por acaso.**

Essa formulação é mais estreita que a original — e por isso mais forte. Ela não pede "um sistema
que leia por mim". Pede **um mecanismo de exposição leve, que não compete com seu modo de
aprendizado reativo, só alimenta o vocabulário dele.**

## 6.4 Atualização da pontuação (doc 04)

| Critério | Antes | Agora | Motivo da mudança |
|---|:---:|:---:|---|
| Frequência | 2 | 2 | Ainda um único evento nomeado com consequência clara |
| Impacto | 2 | 2 | Ainda sem custo mensurável — "entendi tabelas colunares" é ganho, não prejuízo evitado |
| Esforço atual | 1 | 1 | Confirmado: nenhuma tentativa de exposição passiva, nunca |
| Insatisfação | 4 | 4 | Mantida |
| Alternativas | 2 | **1** | Antes eu presumia que alternativas existiam e "não resolviam". Agora sei que **nenhuma foi sequer tentada** — nem a mais barata (RSS, um radar editorial). Isso pesa contra a solução construída, não a favor: o próximo passo mais barato ainda não foi dado. |
| **Total** | 11/25 | **10/25** | |

A nota caiu, mas o motivo pelo qual caiu é o motivo certo: **o próximo passo de menor esforço
(experimentar uma fonte pronta) ainda nem foi tentado.** Isso não é veredito de que o problema é
fraco — é veredito de que **ainda não há dado suficiente para saber**, porque falta testar a coisa
mais óbvia e mais barata primeiro.

## 6.5 Decisão: qual experimento vem agora

O [doc 05](05-decisao-e-experimentos.md) previa dois caminhos a partir do E0: seguir para E1 (se
houvesse consumo represado a testar) ou pular para E2-alt (se o gargalo fosse hábito). **Nenhum dos
dois cenários aconteceu exatamente como previsto** — não há estoque represado (então E1 "puro" não
se aplica do jeito que foi desenhado), e o problema não parece ser falta de hábito de leitura em
geral (você lê bastante, só que sob demanda) — então E2-alt também não encaixa.

O caminho certo agora é uma **versão ajustada do E1**, testando a pergunta que ficou em aberto na
seção 6.2:

### E1′ — Exposição passiva mínima `2 semanas, custo ~0`

**Pergunta:** algo que chega sem que você tenha procurado — é aberto e lido?

**Como:** assinar **2 fontes** (uma newsletter de dados, ex. Data Engineering Weekly; e o
Thoughtworks Technology Radar mais recente, edição única). Não escolher mais que isso. Anotar, por
2 semanas: o que chegou, o que foi aberto, o que foi lido até o fim.

**Por que isso e não pular direto para o concierge (E2):** porque E2 é você mesmo curando 30 min/
semana — isso mede se curadoria manual funciona, mas não separa duas coisas diferentes: "eu leio o
que eu mesmo escolhi" (o que você já faz, no modo pull) de "eu leio o que **chegou até mim sem eu
pedir**" (o que nunca foi testado). E1′ testa exatamente a lacuna nova identificada na seção 6.2.

**Critério de sucesso:** abrir e ler até o fim **pelo menos 3 dos itens** ao longo das 2 semanas.

**Se passar:** siga para o E2 do doc 05 (concierge), já com razoável confiança de que o formato
"chega pronto" funciona para você.

**Se falhar (nada aberto, ou aberto e abandonado):** o achado da seção 6.2 era otimista demais — o
modo pull não é só preferência, é o único modo que funciona para você, e nenhum sistema de entrega
passiva vai mudar isso, por melhor que seja a curadoria. Nesse caso, a resposta certa deixa de ser
"melhorar a entrega" e passa a ser **"melhorar a busca no momento do pull"** — por exemplo, um
hábito leve de, uma vez por trimestre, perguntar a uma IA "o que mudou em [área] desde a última vez
que perguntei" — o que resolve o caso DuckDB sem exigir consumo passivo nenhum.

## 6.6 Veredito atualizado

> ### O problema segue **incerto** — mas agora por um motivo mais preciso.
>
> Não é mais "talvez seja preferência disfarçada de dor" (o E0 afastou isso: não há estoque
> represado, e o modo de aprendizado converte em ação real quando acionado). É "não sabemos se
> exposição passiva funciona para alguém cujo modo de aprendizado é 100% reativo até hoje" — e essa
> é uma pergunta barata e rápida de responder.
>
> **Próximo passo: E1′, 2 semanas, custo zero.** Assinar as 2 fontes citadas hoje e revisar aqui em
> 2 semanas (2026-09-04).
