# 09 — Refinamento do JTBD: dois jobs, não um

Registrado em 2026-08-24, a partir de uma correção direta do usuário: "além de saber coisas novas e
pesquisar, eu gostaria de ver coisas sobre DuckDB, Airflow, etc. Não é só conhecer algo novo, é me
aprofundar, ver artigos e soluções com essas tecnologias."

## 9.1 Os dois jobs

Até o [doc 06](06-resultado-e0.md), o Discovery convergiu para um único job: **"me dê o nome de algo
que eu ainda não conheço"** (Job de Descoberta). Essa correção mostra que existe um segundo job,
igualmente real, que não tinha sido nomeado:

| | **Job de Descoberta** (já mapeado) | **Job de Aprofundamento** (novo, nomeado agora) |
|---|---|---|
| Pergunta que resolve | "O que existe que eu não conheço?" | "O que tem de novo/interessante no que eu **já** uso?" |
| Exemplo | Supabase, mattpocock/skills, DuckDB (primeira vez) | Um novo padrão de particionamento no Airflow, um caso real de uso do DuckDB em produção |
| Evidência já coletada | Forte — 4 casos observados no E0/E1′ (doc 06 §6.6, doc 07) | **Nenhuma ainda** — não apareceu no log até agora |
| Tipo de conteúdo | Nome + 1 linha de contexto basta | Artigo técnico, estudo de caso, comparação de arquitetura — precisa de profundidade |

## 9.2 Por que separar isso importa

Os dois jobs pedem **produtos diferentes**. Um radar bom para descoberta é enxuto (nomes, feed
rápido, grazing) — é o que o doc 06 §6.6 concluiu que já falta pouco para resolver com ferramentas
prontas (YouTube, Substack, comunidades). Um radar bom para aprofundamento precisa filtrar por
**tecnologia específica que você já usa** e trazer profundidade, não novidade — é uma necessidade
de curadoria temática, mais parecida com "me avisa quando sair algo bom sobre X e Y" do que com
"me surpreenda com algo que eu não conheço".

Misturar os dois num único fluxo é o erro mais fácil de cometer aqui: um feed otimizado para
descoberta (superficial, muitos nomes, baixa profundidade) entrega mal o job de aprofundamento; um
feed otimizado para aprofundamento (poucos temas, artigos longos) entrega mal o job de descoberta.

## 9.3 O que ainda falta testar

Esta necessidade foi **declarada agora**, não observada em comportamento — diferente do Job de
Descoberta, que tem 4 casos reais no log. Antes de desenhar solução para ela, vale aplicar o mesmo
cuidado do resto do Discovery: **qual é a evidência mínima de que isso também vira ação, e não só
"seria legal"?**

A partir de agora, ao registrar leituras no [doc 07](07-registro-e1.md), marcar cada item também
com o job que ele serve:

- **[D]** Descoberta — nome novo, tecnologia desconhecida
- **[A]** Aprofundamento — conteúdo novo sobre algo que você já usa/conhece

Isso separa o sinal até 04/09: se, ao ler algo do tipo [A], o mesmo padrão de conversão em ação se
repetir (como aconteceu com Supabase, mattpocock/skills), o Job de Aprofundamento entra confirmado
no MVP. Se não houver nenhum caso [A] até lá, ele fica registrado como requisito declarado, mas
sem teste — decide-se então se vale testar separadamente ou se o produto nasce só para o Job de
Descoberta, que já tem evidência mais forte.

## 9.4 Fontes candidatas para o Job de Aprofundamento (diferente do doc 08)

O [doc 08](08-fontes-candidatas.md) listou fontes para **descoberta** (feeds gerais, formato
grazing). Para aprofundamento, o formato certo é diferente — filtrado por tecnologia específica, não
por tema geral:

- **Busca salva/alerta por tecnologia** — ex. Google Alerts para "DuckDB", "Airflow" — mais barato
  que qualquer fonte nova, testa a demanda antes de construir filtro próprio.
- **Blogs de engenharia de empresas que usam a stack em produção** (Netflix, Airbnb, Uber
  costumam publicar sobre Airflow/orquestração; blog oficial do DuckDB Labs) — conteúdo de
  "solução real", que é exatamente o que foi pedido.
- **Tag/busca dentro do dev.to e Reddit já listados no doc 08**, mas filtrando por nome da
  tecnologia em vez de navegar o feed geral.

Assim como no doc 08, esta lista é ponto de partida, não catálogo final — só entra no MVP se o Job
de Aprofundamento for confirmado por comportamento real, não só pela declaração de hoje.
