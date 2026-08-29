# Auditoria dos vídeos de apresentação — 2026-08-29

## Objetivo

Auditar os sete arquivos de vídeo de apresentação, confirmar a correspondência com os testes de apresentação V02 aprovados, aplicar nomenclatura canônica e registrar a proveniência no repositório.

## Fonte informada

- **Localização correta informada diretamente pelo usuário em 2026-08-29:** `G:\\Meu Drive\\familia_silva\\videos\\apresentação da familia\\`
- O caminho `C:\\Users\\vanze\\OneDrive\\Documentos\\Downloads\\download zz` havia sido informado anteriormente por engano e foi explicitamente corrigido pelo usuário nesta mesma data. Ele **não deve ser usado como fonte desta auditoria**.

## Estado da auditoria

**Status:** `PARCIAL — BLOQUEADA POR ACESSO À FONTE BINÁRIA`

A existência histórica dos sete arquivos abaixo foi registrada na auditoria de `2026-08-28` e em `producao/STATUS.md`. Nesta sessão, o Google Drive conectado ao ChatGPT foi pesquisado pela pasta `apresentação da familia` e também pela forma sem acento `apresentacao da familia`, mas a pasta não foi retornada pela conta/conector disponível. Portanto, ainda não foi possível abrir os binários, conferir quadro/áudio/metadata, calcular hash ou executar o rename físico.

Nenhuma correspondência abaixo deve ser tratada como confirmada somente pelo nome do arquivo. A promoção para `CONFIRMADO` exige inspeção do arquivo real.

## Nomenclatura alvo

Para vídeos individuais de apresentação de personagem, usar:

`VID-CHAR-XXX-APRESENTACAO-VNN.ext`

A primeira versão aprovada desta rodada usa `V01` no **asset de vídeo**, independentemente de a MASTER visual usada na geração ser `V02 PHOTOREALISTIC`.

## Matriz de correspondência candidata

| Nome histórico | Personagem | Teste aprovado | Nome canônico alvo | Estado |
| --- | --- | --- | --- | --- |
| `marcos.mp4` | Marcos Silva (`CHAR-001`) | `TESTE-VIDEO-MARCOS-CHAR-001-002.md` | `VID-CHAR-001-APRESENTACAO-V01.mp4` | `CANDIDATO — NÃO CONFIRMADO POR CONTEÚDO` |
| `celia.mp4` | Dona Célia (`CHAR-002`) | `TESTE-VIDEO-DONA-CELIA-CHAR-002-002.md` | `VID-CHAR-002-APRESENTACAO-V01.mp4` | `CANDIDATO — NÃO CONFIRMADO POR CONTEÚDO` |
| `patricia.mp4` | Patrícia Silva (`CHAR-003`) | `TESTE-VIDEO-PATRICIA-CHAR-003-002.md` | `VID-CHAR-003-APRESENTACAO-V01.mp4` | `CANDIDATO — NÃO CONFIRMADO POR CONTEÚDO` |
| `antonio.mp4` | Sr. Antônio (`CHAR-004`) | `TESTE-VIDEO-ANTONIO-CHAR-004-002.md` | `VID-CHAR-004-APRESENTACAO-V01.mp4` | `CANDIDATO — NÃO CONFIRMADO POR CONTEÚDO` |
| `beto.mp4` | Beto (`CHAR-005`) | `TESTE-VIDEO-BETO-CHAR-005-002.md` | `VID-CHAR-005-APRESENTACAO-V01.mp4` | `CANDIDATO — NÃO CONFIRMADO POR CONTEÚDO` |
| `carol.mp4` | Carol Silva (`CHAR-006`) | `TESTE-VIDEO-CAROL-CHAR-006-002.md` | `VID-CHAR-006-APRESENTACAO-V01.mp4` | `CANDIDATO — NÃO CONFIRMADO POR CONTEÚDO` |
| `dudu.mp4` | Dudu Silva (`CHAR-007`) | `TESTE-VIDEO-DUDU-CHAR-007-001.md` | `VID-CHAR-007-APRESENTACAO-V01.mp4` | `CANDIDATO — NÃO CONFIRMADO POR CONTEÚDO` |

## Critério para confirmação

Para cada arquivo, confirmar no mínimo:

1. personagem visível compatível com a MASTER V02 PHOTOREALISTIC correspondente;
2. vídeo individual de apresentação, não clipe de episódio ou teste anterior;
3. rendering `Photorealistic / Warm Cinematic Realism` consistente com o registro do teste;
4. ausência de evidência de que o arquivo seja uma versão rejeitada ou histórica V01;
5. metadata básica registrada (nome original, tamanho, duração, resolução, fps quando disponível);
6. SHA-256 do binário final após o rename/cópia, quando a fonte física estiver acessível.

## Ação pendente

Assim que a fonte binária `G:\\Meu Drive\\familia_silva\\videos\\apresentação da familia\\` estiver acessível por upload direto, URL/ID de armazenamento conectado ou ambiente com acesso ao caminho montado, abrir os sete vídeos, validar a matriz acima, renomear os arquivos na fonte para os nomes canônicos, registrar hashes/metadata e substituir `Asset de vídeo: A DEFINIR` nos sete registros de teste pela correspondência confirmada.

Até lá, **nenhum `.mp4` foi renomeado, movido, copiado ou ingerido no GitHub nesta auditoria**.
