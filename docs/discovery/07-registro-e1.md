# 07 — Registro do E1′ (exposição passiva mínima)

Decisão registrada em 2026-08-21: **testar antes de construir.** Ver a discussão em
[06 — Resultado do E0](06-resultado-e0.md#65-decisão-qual-experimento-vem-agora) sobre por que o
argumento "construir já me daria disponibilidade" precisa ser testado com algo que já existe antes
de justificar semanas de engenharia — o teste é gratuito, a construção não é.

## Ação de hoje (2026-08-21)

Assinar **2 fontes**, sem escolher mais que isso:

1. **Data Engineering Weekly** — newsletter semanal, foco em engenharia de dados.
2. **Thoughtworks Technology Radar** — edição mais recente (semestral), leitura única.

Consumir do jeito que você descreveu: no caminho do trabalho ou em momentos ociosos, do mesmo jeito
que já consome notícia geral. Não force — o teste é justamente ver se acontece sem esforço extra.

## Critério de sucesso

Abrir e ler até o fim **pelo menos 3 itens** ao longo de 2 semanas.

## Log

Preencher a cada vez que algo chegar e for aberto (ou não):

| Data | Fonte | Item | Abriu? | Leu até o fim? | Observação |
|------|-------|------|--------|-----------------|------------|
| 2026-08-21 | Data Engineering Weekly | [An Ontology for AI Agents is a System](https://www.dataengineeringweekly.com/p/an-ontology-for-ai-agents-is-a-system) | Sim | Sim | Gerou ideia de aplicação real: usar colunas informativas nos datasets para contextualizar regras de negócio, deixando a IA construir métricas mais direcionais em dashboards. |
| 2026-08-22 | Substack (pipeline2insights) | [How to Learn Data Engineering in...](https://pipeline2insights.substack.com/p/how-to-learn-data-engineering-in) | Sim | Sim | Gerou dois planos de ação concretos: projeto público com dados eleitorais (observatório político) e outro com dados públicos do Brasil (observatório de desenvolvimento), como portfólio no GitHub. Também decidiu estudar design system + engenharia de software para freelas de pipeline + frontend. |
| (data não informada, entre 22/08 e hoje) | App Substack (navegação própria) | [50 System Design Concepts Explained](https://designgurus.substack.com/p/50-system-design-concepts-explained) | Sim | **Não** — usuário sinalizou "não entendi muito bem, vou me aprofundar mais" | **Pull, não push** — confirmado pelo usuário: "fui atrás dele por conta própria". Não veio de nenhuma das 2 fontes assinadas. Mas é um pull de um tipo novo: ele instalou o app Substack por causa da assinatura da DEW, e agora **navega dentro dele nos momentos ociosos**, encontrando conteúdo adjacente (system design, engenharia de software) que não teria buscado no Google. Não conta para o critério de sucesso do E1′ (que mede push), mas é dado relevante — ver observação abaixo. |

**2/3 do critério de sucesso atingido em 2 dos 14 dias do experimento** (contando só os itens
via push/assinatura), com reação além do mínimo pedido (leitura completa): os dois itens já
geraram ação planejada, não só interesse. Ver [observação geral](#observação-em-2026-08-22) abaixo.

## Observação em 2026-08-23 (aprox.) — um terceiro modo de descoberta

O item do design system não é push (não veio da newsletter) nem é o pull antigo (não nasceu de um
problema real de trabalho, como todo o histórico do E0). É um modo novo: **navegação exploratória
dentro de um app de descoberta que só existe no celular do usuário porque ele assinou a DEW.**

Isso é um dado potencialmente maior do que os dois itens anteriores, porque sugere uma via mais
barata para o objetivo final do que "construir um coletor do zero": **configurar bem superfícies de
descoberta que já existem** (o feed do próprio Substack, seguir publicações certas, um leitor RSS
com boas fontes) pode já produzir o efeito de navegação ociosa + achado adjacente que o projeto
original queria automatizar. A parte que falta nessa alternativa pronta é **personalização e
recuperação** (Problemas A-refinado e C do doc 06) — não a superfície de descoberta em si.

Vale reter isso para a revisão de 04/09: se o padrão se confirmar, o MVP pode não ser "construir um
crawler", e sim "uma camada fina de captura/organização sobre superfícies de descoberta que já
existem e já funcionam para este usuário".

## Observação em 2026-08-22

Diferença importante em relação a tudo que veio antes deste documento: isto não é mais previsão
("eu abriria..."), é **comportamento real, já registrado**. Isso pesa mais do que qualquer coisa
que os docs 00–06 discutiram.

Dois pontos valem nomear, um positivo e um de atenção:

**Positivo:** os dois itens não pararam em "achei interessante" — cada um puxou uma ideia de
aplicação real, exatamente o padrão identificado na [seção 6.2 do doc 06](06-resultado-e0.md#um-sinal-muito-bom-escondido-na-resposta-4)
(aprendizado convertendo em ação). Se esse ritmo seguir, o critério de sucesso (3 itens lidos até
o fim em 2 semanas) deve ser atingido bem antes do prazo.

**Atenção — não é sobre este experimento, é para depois:** o item de 22/08 já gerou dois projetos
paralelos (observatório político, observatório de desenvolvimento do Brasil) mais um plano de
estudo de design system. Isso é ótimo sinal de conversão em ação — mas também é escopo novo,
diferente do radar de tecnologia. Vale só marcar aqui para não confundir depois: esses projetos são
*efeito* do E1′ funcionando, não *parte* do MVP que este repositório eventualmente construiria. Se
quiser tocá-los, provavelmente merecem repositório próprio.

## Revisão agendada: 2026-09-04

Nessa data, comparar o log com o critério de sucesso:

- **≥3 itens lidos até o fim** → hipótese confirmada. Seguir para o MVP (E3 do
  [doc 05](05-decisao-e-experimentos.md#e3--mvp-mínimo-só-depois-de-e2-passar)) com confiança de
  que o formato "chega pronto" funciona — o próximo trabalho é personalização e recuperação
  (Problemas A-refinado e C), não reprovar a premissa de novo.
- **<3 itens lidos** → a previsão de "eu abriria no caminho do trabalho" não se sustentou mesmo com
  conteúdo tão disponível quanto a notícia geral que você já lê. Nesse caso o gargalo não é
  disponibilidade — é outra coisa (formato, interesse específico, ou o modo pull sendo mesmo o único
  que funciona para você). Revisar com o [doc 06, seção 6.5](06-resultado-e0.md#65-decisão-qual-experimento-vem-agora).
