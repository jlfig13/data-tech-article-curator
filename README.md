# data-tech-article-curator

Radar pessoal de tecnologia para Engenharia de Dados, Análise de Dados, IA aplicada a dados,
Cloud e BI.

## Estado atual: **Discovery. Nada foi construído — de propósito.**

Este repositório está em fase de **Descobrir/Definir** (Double Diamond). A ideia original
(um crawler + classificador + buscador de conteúdo técnico) é tratada aqui como **hipótese de
solução**, não como escopo aprovado.

O E0 (auditoria retrospectiva) já foi respondido e derrubou a hipótese inicial mais provável: não
existe estoque de conteúdo represado (zero newsletters, zero links salvos parados). O padrão real é
outro — **aprendizado 100% reativo (*pull*)**: pesquisa profunda só quando um problema real já está
em mãos, e o que é aprendido costuma virar aplicação real (ex.: DuckDB → tabelas colunares em um
DataLake real). Nunca houve tentativa de exposição passiva a tecnologia (nem a mais barata, como
assinar uma newsletter). **A maior incerteza agora é: algo que chegue pronto, sem você ter ido
atrás, será de fato aberto e lido?** Isso nunca foi testado.

## Documentos

| # | Documento | O que responde |
|---|-----------|----------------|
| 00 | [Hipótese inicial](docs/discovery/00-hipotese-inicial.md) | O que foi pedido, registrado sem edição |
| 01 | [Desconstrução do problema](docs/discovery/01-desconstrucao-do-problema.md) | Pressupostos, reformulação neutra, JTBD |
| 02 | [The Mom Test](docs/discovery/02-mom-test.md) | Roteiro de auto-investigação por comportamento passado |
| 03 | [Alternativas atuais](docs/discovery/03-alternativas-atuais.md) | O que já existe e por que (ainda) não foi usado |
| 04 | [Força do problema](docs/discovery/04-forca-do-problema.md) | Pontuação inicial (11/25), evidências a favor e contra |
| 05 | [Decisão e experimentos](docs/discovery/05-decisao-e-experimentos.md) | Escada de experimentos original (E0 → E3) |
| 06 | [Resultado do E0](docs/discovery/06-resultado-e0.md) | Respostas reais, reformulação do problema, pontuação atualizada (10/25) e próximo experimento (E1′) |
| 07 | [Registro do E1′](docs/discovery/07-registro-e1.md) | Log em andamento — fontes assinadas, itens abertos, revisão em 2026-09-04 |
| 08 | [Fontes candidatas](docs/discovery/08-fontes-candidatas.md) | Lista de fontes-formato-feed para navegação exploratória, escolhidas com base no padrão real observado no E1′ |
| 09 | [Refinamento do JTBD](docs/discovery/09-refinamento-jtbd.md) | Dois jobs distintos: Descoberta (nome novo) x Aprofundamento (conteúdo novo sobre tech já conhecida) |
| 10 | [Fragmentação e agregação](docs/discovery/10-fragmentacao-e-agregacao.md) | Terceiro problema, com evidência real: custo de vigiar várias fontes sem esquecer. Próximo teste: E1″ (agregador RSS pronto) |

## Estado: **em teste, não em construção**

Decisão de 2026-08-21: **testar antes de construir.** Duas fontes prontas foram assinadas
(sem código, sem custo). O critério que decide se o MVP começa a ser construído está em
[07 — Registro do E1′](docs/discovery/07-registro-e1.md): ler até o fim ≥3 itens em 2 semanas.
Revisão marcada para **2026-09-04**.

## Leitura mínima

Se for ler só uma coisa: [07 — Registro do E1′](docs/discovery/07-registro-e1.md).
