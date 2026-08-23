# 11 — Lista de feeds para o E1″ (agregador RSS)

Lista pronta para colar no Feedly, Inoreader ou qualquer leitor RSS. URLs confirmadas por busca em
2026-08-24 — ver fontes ao final de cada grupo. Faz parte do teste descrito no
[doc 10](10-fragmentacao-e-agregacao.md#104-próximo-experimento-e1-agregador-pronto-20-min-de-setup-resto-do-prazo-até-04-09).

## Grupo 1 — Descoberta [D] e Aprofundamento [A] combinados

| Feed | URL | Job |
|---|---|---|
| Data Engineering Weekly | `https://www.dataengineeringweekly.com/feed` | D + A |
| Blog oficial do DuckDB | `http://duckdb.org/feed.xml` | A |
| Netflix Tech Blog | `https://netflixtechblog.com/feed` | A (casos reais de dados/streaming em produção) |
| Airbnb Engineering (Medium) | `https://medium.com/feed/airbnb-engineering` | A |

## Grupo 2 — dev.to por tag (Aprofundamento [A], filtrado por tecnologia)

Formato: `https://dev.to/feed/tag/<tag>`

| Feed | URL |
|---|---|
| Tag `dataengineering` | `https://dev.to/feed/tag/dataengineering` |
| Tag `airflow` | `https://dev.to/feed/tag/airflow` |
| Tag `duckdb` | `https://dev.to/feed/tag/duckdb` |

## Grupo 3 — GitHub Trending (Descoberta [D])

Gerador de feed não-oficial, mantido no GitHub, com páginas por linguagem:
`https://mshibanami.github.io/GitHubTrendingRSS/`

Abra o link acima e copie a URL da linguagem que fizer mais sentido para você (ex. Python, SQL) —
o próprio site já lista as URLs de feed prontas por linguagem.

## Grupo 4 — Google Alerts (Aprofundamento [A], sem URL fixa — precisa criar)

Não tem link pronto porque é por conta do usuário. Passo a passo:

1. Acesse [google.com/alerts](https://www.google.com/alerts)
2. Crie um alerta para `DuckDB` e outro para `Apache Airflow`
3. Em "Como enviar", escolha **"Feed RSS"** em vez de e-mail
4. Copie a URL do feed gerado e cole no agregador

## O que fica de fora (de propósito)

- **Substack** — não entra como feed porque o comportamento que está funcionando para você é
  navegar dentro do app (grazing), não ler item por item num agregador. Ver
  [doc 07](07-registro-e1.md#log--navegação-exploratória-fora-do-critério-push-registrado-à-parte).
- **YouTube** — mesma lógica: o algoritmo de sugestão já está entregando resultado (caso
  mattpocock/skills). Puxar isso pra um RSS via ID de canal só faria sentido se você já soubesse
  quais canais específicos seguir — o que ainda não é o caso.
- **LinkedIn** — não expõe RSS. Fica de fora por limitação da própria plataforma, sem alternativa
  gratuita confiável.

## Como usar

Cole os feeds dos Grupos 1–3 direto no Feedly/Inoreader (a maioria dos leitores aceita "Add feed by
URL"). Crie o Google Alerts do Grupo 4 e adicione o link gerado. Depois disso, o teste é simples:
abrir esse agregador em vez de abrir cada fonte separadamente, e registrar no
[doc 10](10-fragmentacao-e-agregacao.md) se isso reduziu a sensação de estar perdendo algo.
