# Continuidade

Este documento define o estado que precisa ser preservado entre episódios, temporadas, imagens, vídeos, vozes e narrativas.

## Cânone

Cânone é toda informação aprovada e registrada oficialmente. Não são cânone:

- informações marcadas como `A DEFINIR`;
- hipóteses e ideias em rascunho;
- prompts experimentais;
- imagens ou vídeos não aprovados na dimensão citada;
- voz, diálogo ou dinâmica narrativa presentes em um teste aprovado somente no visual.

## Estado consolidado em 2026-08-28

### Personagens

| ID | Personagem | Personalidade | Visual | Voz |
| --- | --- | --- | --- | --- |
| [`CHAR-001`](../personagens/oficiais/CHAR-001-MARCOS.md) | Marcos Silva | `CANÔNICA` | `APROVADO COM RESSALVAS` | `A DEFINIR` |
| [`CHAR-002`](../personagens/oficiais/CHAR-002-DONA-CELIA.md) | Dona Célia | `CANÔNICA` | `APROVADO COM RESSALVAS` | `A DEFINIR` |
| [`CHAR-003`](../personagens/oficiais/CHAR-003-PATRICIA-SILVA.md) | Patrícia Silva | `CANÔNICA` | `APROVADO COM RESSALVAS` | `A DEFINIR` |
| [`CHAR-004`](../personagens/oficiais/CHAR-004-ANTONIO-SILVA.md) | Sr. Antônio | `CANÔNICA` | `APROVADO COM RESSALVAS` | `A DEFINIR` |
| [`CHAR-005`](../personagens/oficiais/CHAR-005-BETO.md) | Beto | `CANÔNICA` | `APROVADO COM RESSALVAS` | `A DEFINIR` |
| [`CHAR-006`](../personagens/oficiais/CHAR-006-CAROL-SILVA.md) | Carol Silva | `CANÔNICA` | `APROVADO VISUALMENTE` | `A DEFINIR` |
| [`CHAR-007`](../personagens/oficiais/CHAR-007-DUDU-SILVA.md) | Dudu Silva | `CANÔNICA` | `AJUSTE NECESSÁRIO` | `A DEFINIR` |

Os IDs não podem ser reutilizados ou renumerados. As personalidades completas estão em [../personagens/oficiais/personalidades/](../personagens/oficiais/personalidades/).

### Rendering permanente

`Photorealistic / Warm Cinematic Realism` é o padrão canônico pela [DEC-003](DECISOES.md#dec-003). Ele substitui direções anteriores de cartoon ou realismo estilizado quando houver contradição.

### Referências visuais

- Cada personagem usa somente sua própria imagem MASTER ou referência aprovada.
- A imagem MASTER continua sendo a referência facial primária.
- Um vídeo pode complementar somente a dimensão explicitamente aprovada.
- Sr. Antônio e Beto são referências metodológicas de arquitetura de prompt e rendering, nunca referências faciais de outros personagens.
- Os nomes de arquivos informados nas fichas ainda precisam ser versionados em [../assets/personagens/](../assets/personagens/).
- A referência de Dudu precisa ser refeita sem gimbal/celular, com boca fechada e tênis sem marca.

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

Cada episódio aprovado deve registrar:

- Episódio: `S01E001`.
- Evento: `A DEFINIR`.
- Impacto futuro: `A DEFINIR`.
- Status: `A DEFINIR`.

## Objetos e layout

Objetos recorrentes devem registrar nome, local, dono/usuário, episódios e regras de continuidade. Quando a casa principal for aprovada, registrar ambientes, posições relativas, portas, janelas, corredores, móveis, objetos e regras visuais.

## Voz e personalidade

Cada voz futura deve ter versão, fonte, ritmo, vínculo exclusivo, teste e aprovação específica. A personalidade e os limites de comportamento continuam definidos nos documentos canônicos, mesmo quando a voz ainda está `A DEFINIR`.
