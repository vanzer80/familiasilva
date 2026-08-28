# Continuidade

Este documento define o estado que precisa ser preservado entre episódios, temporadas, imagens, vídeos, vozes e narrativas.

## Cânone

Cânone é toda informação aprovada e registrada oficialmente. Não são cânone:

- informações marcadas como `A DEFINIR`;
- hipóteses e ideias em rascunho;
- prompts experimentais;
- imagens ou vídeos não aprovados na dimensão citada;
- voz, diálogo ou dinâmica narrativa presentes em um teste aprovado somente no visual.

## Estado consolidado em 2026-08-28 (reconciliado)

### Personagens

| ID | Personagem | Personalidade | Visual | Voz |
| --- | --- | --- | --- | --- |
| [`CHAR-001`](../personagens/oficiais/CHAR-001-MARCOS.md) | Marcos Silva | `CANÔNICA` | `APROVADO / CANON VISUAL PARA RENDERING DE VIDEO` | `A DEFINIR` |
| [`CHAR-002`](../personagens/oficiais/CHAR-002-DONA-CELIA.md) | Dona Célia | `CANÔNICA` | `APROVADO / CANON VISUAL PARA RENDERING DE VIDEO` | `A DEFINIR` |
| [`CHAR-003`](../personagens/oficiais/CHAR-003-PATRICIA-SILVA.md) | Patrícia Silva | `CANÔNICA` | `APROVADO / CANON VISUAL PARA RENDERING DE VIDEO` (V02 PHOTOREALISTIC — current canon; V01 histórica) | `A DEFINIR` |
| [`CHAR-004`](../personagens/oficiais/CHAR-004-ANTONIO-SILVA.md) | Sr. Antônio | `CANÔNICA` | `APROVADO / CANON VISUAL` (referência metodológica) | `A DEFINIR` |
| [`CHAR-005`](../personagens/oficiais/CHAR-005-BETO.md) | Beto | `CANÔNICA` | `APROVADO / CANON VISUAL EM VIDEO` | `A DEFINIR` |
| [`CHAR-006`](../personagens/oficiais/CHAR-006-CAROL-SILVA.md) | Carol Silva | `CANÔNICA` | `APROVADO VISUALMENTE` | `A DEFINIR` |
| [`CHAR-007`](../personagens/oficiais/CHAR-007-DUDU-SILVA.md) | Dudu Silva | `CANÔNICA` | `APROVADO / CANON VISUAL` (ver observação técnica em ERR-006) | `A DEFINIR` |

Os IDs não podem ser reutilizados ou renumerados. As personalidades completas estão em [../personagens/oficiais/personalidades/](../personagens/oficiais/personalidades/). Os status visuais acima foram reconciliados pela [DEC-013](DECISOES.md#dec-013) a partir de duas linhas de decisão independentes (DEC-002/DEC-005 e DEC-009/DEC-011/DEC-012); ver nota de reconciliação em DECISOES.md.

### Rendering permanente

`Photorealistic / Warm Cinematic Realism` é o padrão canônico pela [DEC-003](DECISOES.md#dec-003). Ele substitui direções anteriores de cartoon ou realismo estilizado quando houver contradição.

### Referências visuais

- Cada personagem usa somente sua própria imagem MASTER ou referência aprovada.
- A imagem MASTER continua sendo a referência facial primária.
- Um vídeo pode complementar somente a dimensão explicitamente aprovada.
- Sr. Antônio e Beto são referências metodológicas de arquitetura de prompt e rendering, nunca referências faciais de outros personagens.
- As sete imagens MASTER `V02 PHOTOREALISTIC` são a referência visual `CURRENT CANON` desde `2026-08-28` ([DEC-015](DECISOES.md#dec-015)) e estão versionadas em [../assets/personagens/mestres/](../assets/personagens/mestres/), catalogadas em [MANIFESTO-MESTRES.md](../assets/personagens/mestres/MANIFESTO-MESTRES.md). As sete MASTERs `V01` (pela `DEC-014`) permanecem preservadas como `HISTORICAL` e não devem ser escolhidas automaticamente para novas gerações.
- A referência atual de Dudu está aprovada como canon visual (`DEC-013`), mas contém elementos a evitar em referências futuras (gimbal/celular, boca aberta, tênis de marca) — ver `ERR-006` e `SOL-006`; esse ponto não foi encerrado pela V02.
- As sete MASTERs V02 PHOTOREALISTIC foram validadas em vídeo (apresentação individual) no Google Flow em `2026-08-28`, com aprovação do usuário para os sete personagens; ver registros `producao/testes/TESTE-VIDEO-*-CHAR-00X-002.md` (Dudu: `-001`, primeiro teste de vídeo dele). Essa validação cobre apenas rendering e identidade visual — voz, fala final exata e dinâmica narrativa não foram aprovadas por esses testes.

### Relações permanentes

- Marcos e Patrícia são casados.
- Carol e Dudu são filhos de Marcos e Patrícia e irmãos entre si.
- Carol e Beto são casados.
- Dona Célia é mãe de Marcos, sogra de Patrícia e avó de Carol e Dudu.
- Beto é genro de Marcos e Patrícia e cunhado de Dudu.
- Sr. Antônio é vizinho recorrente e não integra oficialmente a Família Silva.
- A paixonite de Sr. Antônio por Patrícia é platônica, unilateral e não correspondida.
- A relação entre Sr. Antônio e Marcos inclui rivalidade e inveja cômica leve.

A matriz bidirecional está em [../personagens/relacoes/RELACOES-FAMILIARES.md](../personagens/relacoes/RELACOES-FAMILIARES.md).

## Continuidade de vídeo

Todo novo prompt deve seguir [../prompts/templates/TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md) e as regras em [../personagens/regras/](../personagens/regras/).

Devem ser preservadas separadamente:

- aparência do personagem;
- rendering da série;
- figurino;
- ambiente;
- relacionamento;
- fala;
- voz;
- lip sync;
- silêncio de personagens sem fala.

## Eventos anteriores

### S01E001 — A Greve da Patrícia

Importado em `2026-08-28` de [FONTE-HISTORICA-S01E001-A-GREVE-DA-PATRICIA.md](../episodios/S01/FONTE-HISTORICA-S01E001-A-GREVE-DA-PATRICIA.md). Eventos diretamente sustentados pelo roteiro:

| Evento | Cena | Impacto futuro | Status |
| --- | --- | --- | --- |
| Beto deve R$50 a um primo e usa uma falsa "reunião de negócios" para conseguir salgadinhos de Patrícia | 2 | Beto tem uma dívida pessoal preexistente com um primo; pode ser retomada em episódios futuros | `NO ROTEIRO APROVADO` |
| Patrícia declara greve doméstica (para de procurar, lembrar, preparar e resolver por todos) | 3 | Marco de virada da dinâmica familiar; pode ser referenciada como precedente | `NO ROTEIRO APROVADO` |
| Marcos cria uma "escala doméstica" que a família tenta contornar cômicamente | 9 | Estabelece o padrão de Marcos responder a problemas emocionais com soluções organizacionais | `NO ROTEIRO APROVADO` |
| Sr. Antônio elogia a aparência de Patrícia; Marcos reage com ciúme cômico leve | 7–8 | Consistente com a personalidade canônica de Sr. Antônio (paixonite platônica não correspondida) e com a rivalidade cômica leve com Marcos | `NO ROTEIRO APROVADO` |
| Marcos reconhece que tratou cuidar da casa como substituto de atenção emocional; reconciliação com Patrícia | 11–12 | Pequeno avanço emocional do casal, sem "curar" os personagens — pode ser referenciado em episódios futuros | `NO ROTEIRO APROVADO` |

**Status `NO ROTEIRO APROVADO`** indica que o evento está sustentado pelo roteiro-fonte fornecido pelo usuário, distinto de confirmação de que os 29 clipes foram efetivamente gerados e aprovados em vídeo (isso seguiria o fluxo normal em `producao/testes/` → `producao/aprovados/`, ainda não registrado clipe a clipe para este episódio, exceto a Cena 2B — ver `ERR-007`/`SOL-007`).

### Template de entrada para novos episódios

- Episódio: `S01E001`.
- Evento: `A DEFINIR`.
- Impacto futuro: `A DEFINIR`.
- Status: `A DEFINIR`.

## Objetos e layout

Objetos recorrentes devem registrar nome, local, dono/usuário, episódios e regras de continuidade. Quando a casa principal for aprovada, registrar ambientes, posições relativas, portas, janelas, corredores, móveis, objetos e regras visuais.

## Voz e personalidade

Cada voz futura deve ter versão, fonte, ritmo, vínculo exclusivo, teste e aprovação específica. A personalidade e os limites de comportamento continuam definidos nos documentos canônicos, mesmo quando a voz ainda está `A DEFINIR`.
