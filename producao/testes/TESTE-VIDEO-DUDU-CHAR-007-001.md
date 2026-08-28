# TEST-VIDEO-CHAR-007-001 — Dudu

- **Data:** `2026-08-28`
- **Personagem:** Dudu Silva (`CHAR-007`)
- **Rodada:** validação da MASTER V02 PHOTOREALISTIC em vídeo — apresentação individual. Primeiro teste de **vídeo** de Dudu neste repositório (distinto de [TESTE-REFERENCIA-DUDU-CHAR-007-001.md](TESTE-REFERENCIA-DUDU-CHAR-007-001.md), que avaliou apenas a imagem de referência V01).
- **MASTER usada:** `IMG-CHAR-007-DUDU-SILVA-MASTER-V02-PHOTOREALISTIC.jpeg` (current canon — [DEC-015](../../docs/DECISOES.md#dec-015))
- **Ferramenta:** Google Flow
- **Objetivo:** vídeo individual de apresentação
- **Estado visual:** `APROVADO`
- **Ferramenta/configuração exata:** `A DEFINIR`
- **Prompt exato:** `A DEFINIR`
- **Fala final / diálogo exato:** `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` — o usuário informou ter feito pequenas alterações manuais na fala antes da geração; o texto literal final não está disponível como fonte verificável neste repositório. Não reconstruir por suposição.
- **Asset de vídeo:** `A DEFINIR`. Possível correspondência não confirmada com arquivo nomeado por personagem encontrado em `G:\Meu Drive\familia_silva\videos\` durante auditoria de `2026-08-28` (ver `producao/STATUS.md`); não vinculado formalmente até confirmação.

## Tentativa inicial bloqueada (FATO)

A primeira tentativa de geração foi bloqueada pelo Google Flow com a mensagem "Esse comando pode violar nossas políticas contra a geração de imagens de pessoas famosas." Não houve cobrança pela geração bloqueada. Ver [ERR-008](../erros/ERR-008-FLOW-FALSO-POSITIVO-PESSOA-FAMOSA.md).

## Correção aplicada e resultado

O prompt foi reformulado com contexto ficcional/compliance simplificado (personagem ficcional original, referência pertencente ao projeto, sem intenção de retratar pessoa real), mantendo sem enfraquecer o requisito de live-action photorealistic e evitando linguagem biométrica rígida — ver [SOL-008](../solucoes/SOL-008-CONTEXTO-FICCIONAL-COMPLIANCE-FLOW.md). Após essa reformulação, a geração funcionou. **Fato:** o bloqueio desapareceu após a reformulação do prompt. **Não comprovado:** a causa exata interna do classificador do Flow; não afirmar que o motivo foi a aparência do personagem se assemelhar a alguma pessoa famosa — isso é apenas hipótese não confirmada.

A geração resultante apresentou `Photorealistic / Warm Cinematic Realism`: pessoa real filmada, sem cartoon, sem 3D/CGI. Somente Dudu estava em foco/visível na cena. A identidade visual foi considerada consistente com a MASTER V02 PHOTOREALISTIC do personagem. O usuário analisou o vídeo e aprovou o resultado; não houve necessidade de refazer a geração.

## Nota sobre a pendência de referência neutra (ERR-006/SOL-006)

A referência usada nesta geração foi a MASTER V02 PHOTOREALISTIC, verificada durante a migração de `2026-08-28` como sem gimbal/celular em quadro e com boca fechada. O calçado não é visível no enquadramento dessa imagem, portanto esse ponto específico de `ERR-006` continua **não confirmável** (nem como problema, nem como resolvido) a partir da MASTER V02. A recomendação de `SOL-006` de produzir/aprovar uma referência neutra dedicada continua válida e não é encerrada por este teste.

## Impacto no cânone

Aprovação desta geração específica (rendering fotorrealista + identidade visual V02 + vídeo individual de apresentação). Este teste **não** amplia automaticamente aprovação de voz, fala final exata ou dinâmica narrativa — essas dimensões permanecem `A DEFINIR`/pendentes até aprovação explícita separada. Não revoga nem encerra `ERR-006`/`SOL-006`. Reforça a evidência já registrada em [LRN-013](../../docs/APRENDIZADOS-DE-VIDEO.md) e o novo fallback registrado em [LRN-014](../../docs/APRENDIZADOS-DE-VIDEO.md).
