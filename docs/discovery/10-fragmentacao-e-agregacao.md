# 10 — Fragmentação: um terceiro problema, com evidência real

Registrado em 2026-08-24. Reação direta do usuário depois de alguns dias vivendo a rotina proposta
no E1′:

> "Você vê que eu preciso ficar acessando várias ferramentas descentralizadas, ir no Substack, ir
> no LinkedIn, ir no YouTube, ir no blog oficial do DuckDB, ir no meu e-mail só para verificar se
> há novidade — é exatamente o que queria evitar. Esperar a notícia vir por diversos meios
> desordenados e aleatórios. Isso funciona, mas na sorte, posso estar deixando passar algo
> importante simplesmente por esquecer vários dias sem consultar. A ideia é criar em um único
> lugar e eu poder ler e escolher o que achei interessante em acrescentar no meu conhecimento."

## 10.1 Por que isso é diferente de tudo que veio antes

Até aqui, o Discovery tinha respondido duas perguntas com evidência forte:

1. **Existe conteúdo relevante disponível?** Sim ([doc 08](08-fontes-candidatas.md)).
2. **Você lê e aplica quando o conteúdo aparece?** Sim, muito bem — 5 casos com conversão em ação
   real ([doc 07](07-registro-e1.md)).

Faltava uma terceira pergunta, que só pôde aparecer porque você **viveu** o processo manual nos
últimos dias: **o custo de vigiar várias fontes, sem esquecer, é sustentável?**

A resposta que você acabou de dar é não — e isso não é mais previsão ("eu abriria..."), é reflexão
sobre um comportamento que você mesmo executou por vários dias. Isso conta como evidência de
**esforço real e insatisfação com esse esforço**, o critério que estava mais fraco em toda a análise
desde o [doc 04](04-forca-do-problema.md#41-pontuação-1-a-5) (nota 1/5 em "esforço atual" — porque
antes do E1′ você simplesmente não tentava nada). Agora existe uma tentativa real, e ela revelou um
custo específico e nomeável: **checar N lugares sem esquecer nenhum**.

## 10.2 O problema reformulado (3ª versão)

> **Você tem fontes de descoberta que funcionam individualmente (Substack, YouTube, e-mail, blog do
> DuckDB) — mas mantê-las sob vigilância simultânea depende inteiramente da sua memória e disciplina
> para abrir cada uma delas. Como não há garantia de checar todas com regularidade, existe risco real
> de perder algo relevante por simples esquecimento, não por falta de conteúdo ou desinteresse.**

Isso é o **Problema de Consolidação** — não estava nomeado nos docs 01–09. Ele não substitui a
Descoberta [D] nem o Aprofundamento [A]; é ortogonal a ambos — é sobre **onde você olha**, não
sobre o que você acha quando olha.

## 10.3 Antes de construir: existe versão pronta?

A disciplina do Discovery até aqui sempre foi a mesma: testar o que já existe, de graça, antes de
justificar construção. Aqui a resposta pronta tem nome — **leitor de RSS/agregador** (Feedly,
Inoreader, ou similar). A maioria das fontes já mapeadas tem feed RSS:

| Fonte | Tem RSS/alerta agregável? |
|---|---|
| Data Engineering Weekly | Sim |
| Blog do DuckDB Labs | Sim |
| Blogs de engenharia (Airflow em produção) | Normalmente sim |
| Google Alerts (DuckDB, Airflow) | Sim — o próprio Alerts gera feed |
| GitHub Trending | Sim, via bridges gratuitos ou repositórios "awesome" com feed |
| Canais do YouTube | Sim — todo canal tem feed RSS próprio |
| Substack (grazing no app) | **Não de forma limpa** — é navegação dentro do app, não dá pra
  agregar como feed sem perder o formato que já está funcionando bem para você |
| LinkedIn | **Não** — não expõe RSS, é a fonte mais fechada da lista |

Ou seja: **quase tudo que você está checando manualmente pode cair num único agregador, exceto o
Substack (que já é "um lugar único" para grazing) e o LinkedIn** (que fica de fora por limitação
técnica da própria plataforma, não por escolha).

## 10.4 Próximo experimento: E1″ — Agregador pronto `~20 min de setup, resto do prazo até 04/09`

**Pergunta:** um único ponto de checagem (RSS) resolve o "esquecimento" sem eu precisar construir
nada?

**Como:**
1. Criar conta gratuita em um agregador (Feedly ou Inoreader).
2. Adicionar os feeds da tabela acima que tiverem RSS: DEW, blog do DuckDB, 1 blog de engenharia
   sobre Airflow, Google Alerts para "DuckDB" e "Airflow", GitHub Trending (filtrado por linguagem
   relevante).
3. Continuar usando Substack e YouTube como já estava (eles não entram no agregador — continuam
   sendo canais de descoberta separados, e está tudo bem, porque já funcionam).
4. Nos dias que restam até 04/09, checar o agregador em vez de abrir e-mail/blog um por um, e
   registrar aqui se isso reduziu a sensação de "posso estar perdendo algo".

**Critério de sucesso:** você abre o agregador com regularidade (não precisa ser diário) e sente
que checar "um lugar a menos para lembrar" já ajuda — mesmo que Substack e YouTube continuem
separados.

**Se funcionar:** o Problema de Consolidação está parcialmente resolvido por ferramenta pronta, e o
que resta para um eventual MVP fica ainda mais estreito: **um agregador pessoal só faria sentido
construir se ele também conseguisse (a) capturar achados do Substack/YouTube que o RSS não alcança,
e (b) aplicar os filtros [D]/[A] do doc 09** — coisas que Feedly não faz por padrão. Isso vira a
especificação real do MVP, não mais uma suposição.

**Se não funcionar** (você ainda esquece de checar, mesmo com tudo num só lugar): o problema não é
fragmentação de fontes, é falta de **empurrão ativo** (notificação, lembrete) — nesse caso a
resposta certa é diferente: não é juntar fontes, é criar um gatilho de tempo (ex. um lembrete
semanal fixo), o que é uma solução completamente diferente e muito mais barata que qualquer
agregador.

## 10.5 Nota sobre o veredito geral

Isso muda a leitura da revisão de 04/09: em vez de decidir só "o Job de Descoberta funciona, sim/
não", agora há três perguntas para responder naquele dia — Descoberta [D] (já com evidência forte),
Aprofundamento [A] (ainda sem evidência), e Consolidação (este documento, teste em andamento). O
MVP, se vier a existir, provavelmente não nasce para resolver todas as três ao mesmo tempo — nasce
para a que tiver a evidência mais forte E o menor "já resolvido por ferramenta pronta".
