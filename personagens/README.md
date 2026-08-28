# Personagens

Este diretório é o cadastro canônico dos personagens da série Família Silva. IDs e nomes foram aprovados na [DEC-002](../docs/DECISOES.md#dec-002).

## Cadastro e estado

| ID | Nome oficial | Nome de uso | Ficha | Personalidade | Estado visual |
| --- | --- | --- | --- | --- | --- |
| `CHAR-001` | Marcos Silva | Marcos | [Ficha](oficiais/CHAR-001-MARCOS.md) | [Canônica](oficiais/personalidades/MARCOS-PERSONALIDADE.md) | `APROVADO COM RESSALVAS` |
| `CHAR-002` | Dona Célia | Dona Célia | [Ficha](oficiais/CHAR-002-DONA-CELIA.md) | [Canônica](oficiais/personalidades/DONA-CELIA-PERSONALIDADE.md) | `APROVADO COM RESSALVAS` |
| `CHAR-003` | Patrícia Silva | Patrícia | [Ficha](oficiais/CHAR-003-PATRICIA-SILVA.md) | [Canônica](oficiais/personalidades/PATRICIA-PERSONALIDADE.md) | `APROVADO COM RESSALVAS` |
| `CHAR-004` | Antônio Silva | Sr. Antônio | [Ficha](oficiais/CHAR-004-ANTONIO-SILVA.md) | [Canônica](oficiais/personalidades/ANTONIO-PERSONALIDADE.md) | `APROVADO COM RESSALVAS` |
| `CHAR-005` | Beto | Beto | [Ficha](oficiais/CHAR-005-BETO.md) | [Canônica](oficiais/personalidades/BETO-PERSONALIDADE.md) | `APROVADO COM RESSALVAS` |
| `CHAR-006` | Carol Silva | Carol | [Ficha](oficiais/CHAR-006-CAROL-SILVA.md) | [Canônica](oficiais/personalidades/CAROL-PERSONALIDADE.md) | `APROVADO VISUALMENTE` |
| `CHAR-007` | Dudu Silva | Dudu | [Ficha](oficiais/CHAR-007-DUDU-SILVA.md) | [Canônica](oficiais/personalidades/DUDU-PERSONALIDADE.md) | `AJUSTE NECESSÁRIO` |

Antônio Silva é conhecido como Sr. Antônio. Seu sobrenome não altera sua posição: ele é vizinho recorrente e não integra oficialmente a Família Silva. O nome oficial de `CHAR-005` é apenas **Beto**.

## Referências visuais informadas

| Personagem | Nome informado | Situação no repositório |
| --- | --- | --- |
| Marcos | `marcos_silva.jpeg` | arquivo ainda não versionado |
| Dona Célia | `celia_silva.png` | arquivo ainda não versionado |
| Patrícia | `patricia_silva.png` | arquivo ainda não versionado |
| Sr. Antônio | `antonio_silva.png` | arquivo ainda não versionado |
| Beto | `beto.png` | arquivo ainda não versionado |
| Carol | `carol_silva.png` | referência primária aprovada; arquivo ainda não versionado |
| Dudu | `dudu_silva.png` | precisa ser refeita antes da aprovação |

Nome informado não equivale a asset versionado. O Asset ID e o caminho oficial só podem ser preenchidos depois que o arquivo for adicionado a [../assets/personagens/](../assets/personagens/).

## Regras permanentes

- Nunca reutilizar ou renumerar um Character ID.
- Cada personagem usa somente sua própria imagem MASTER ou referência aprovada.
- Vídeo aprovado complementa somente a dimensão declarada.
- Antônio e Beto são referências metodológicas, nunca faciais para os demais.
- Voz precisa de aprovação específica.
- Campos sem fonte continuam `A DEFINIR`.
- Aparência visual segue `Photorealistic / Warm Cinematic Realism`.

## Como criar um personagem

1. Reservar o próximo ID sem reutilizar números.
2. Copiar [templates/TEMPLATE-PERSONAGEM.md](templates/TEMPLATE-PERSONAGEM.md).
3. Preencher apenas informações aprovadas.
4. Usar `A DEFINIR` para campos indefinidos.
5. Vincular uma imagem MASTER somente depois de aprovação e versionamento do asset.
6. Atualizar [../docs/CONTINUIDADE.md](../docs/CONTINUIDADE.md), changelog e decisões quando aplicável.
