# Personagens

Este diretório é o cadastro canônico dos personagens da série Família Silva. IDs e nomes foram aprovados na [DEC-002](../docs/DECISOES.md#dec-002).

## Cadastro e estado

| ID | Nome oficial | Nome de uso | Ficha | Personalidade | Estado visual |
| --- | --- | --- | --- | --- | --- |
| `CHAR-001` | Marcos Silva | Marcos | [Ficha](oficiais/CHAR-001-MARCOS.md) | [Canônica](oficiais/personalidades/MARCOS-PERSONALIDADE.md) | `APROVADO / CANON VISUAL` |
| `CHAR-002` | Dona Célia | Dona Célia | [Ficha](oficiais/CHAR-002-DONA-CELIA.md) | [Canônica](oficiais/personalidades/DONA-CELIA-PERSONALIDADE.md) | `APROVADO / CANON VISUAL` |
| `CHAR-003` | Patrícia Silva | Patrícia | [Ficha](oficiais/CHAR-003-PATRICIA-SILVA.md) | [Canônica](oficiais/personalidades/PATRICIA-PERSONALIDADE.md) | `APROVADO / CANON VISUAL` (V02 PHOTOREALISTIC — current canon) |
| `CHAR-004` | Sr. Antônio (nome de arquivo legado: Antônio Silva) | Sr. Antônio | [Ficha](oficiais/CHAR-004-ANTONIO-SILVA.md) | [Canônica](oficiais/personalidades/ANTONIO-PERSONALIDADE.md) | `APROVADO / CANON VISUAL` |
| `CHAR-005` | Beto | Beto | [Ficha](oficiais/CHAR-005-BETO.md) | [Canônica](oficiais/personalidades/BETO-PERSONALIDADE.md) | `APROVADO / CANON VISUAL` |
| `CHAR-006` | Carol Silva | Carol | [Ficha](oficiais/CHAR-006-CAROL-SILVA.md) | [Canônica](oficiais/personalidades/CAROL-PERSONALIDADE.md) | `APROVADO VISUALMENTE` |
| `CHAR-007` | Dudu Silva | Dudu | [Ficha](oficiais/CHAR-007-DUDU-SILVA.md) | [Canônica](oficiais/personalidades/DUDU-PERSONALIDADE.md) | `APROVADO / CANON VISUAL` (ver `ERR-006`) |

Status visuais reconciliados pela [DEC-013](../docs/DECISOES.md#dec-013) em `2026-08-28`. Antônio Silva é conhecido como Sr. Antônio; esse é o nome canônico a ser usado em roteiro e prompts — o sobrenome "Silva" permanece apenas como identificador técnico legado no nome do arquivo e do asset, e não altera sua posição: ele é vizinho recorrente e não integra oficialmente a Família Silva. O nome oficial de `CHAR-005` é apenas **Beto**.

## Imagens MASTER

As sete imagens MASTER `V02 PHOTOREALISTIC` do elenco inicial são a referência visual `CURRENT CANON` desde `2026-08-28` ([DEC-015](../docs/DECISOES.md#dec-015)) e estão versionadas em [../assets/personagens/mestres/](../assets/personagens/mestres/), catalogadas com SHA-256 e proveniência em [MANIFESTO-MESTRES.md](../assets/personagens/mestres/MANIFESTO-MESTRES.md). As sete imagens `V01` (pela [DEC-014](../docs/DECISOES.md#dec-014)) permanecem preservadas como `HISTORICAL` e não devem ser escolhidas automaticamente para novas gerações.

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
