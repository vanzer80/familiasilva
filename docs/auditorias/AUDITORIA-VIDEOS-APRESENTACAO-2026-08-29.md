# Auditoria dos vídeos de apresentação — 2026-08-29

## Objetivo

Auditar os sete arquivos de vídeo de apresentação, confirmar a correspondência com os testes de apresentação V02 aprovados, aplicar nomenclatura canônica e registrar a proveniência no repositório.

## Fonte confirmada

- **Localização correta:** `G:\\Meu Drive\\familia_silva\\videos\\apresentação da familia\\`
- **Google Drive folder ID:** `1VuZvtH8MY1NDAwbVcQKLH1_bVrWV4rc8`

O caminho `C:\\Users\\vanze\\OneDrive\\Documentos\\Downloads\\download zz` havia sido informado anteriormente por engano e foi explicitamente corrigido pelo usuário em `2026-08-29`. Ele não pertence a esta auditoria.

## Estado da auditoria

**Status:** `CONTEÚDO E CORRESPONDÊNCIA CONFIRMADOS — RENAME FÍSICO PENDENTE`

Em `2026-08-29`, a pasta correta tornou-se acessível pelo Google Drive conectado. Foram localizados exatamente sete vídeos de apresentação. Os sete binários foram baixados e inspecionados por amostragem visual de múltiplos frames, comparados com as MASTERs V02 PHOTOREALISTIC correspondentes e analisados tecnicamente com `ffprobe`.

A correspondência personagem ↔ vídeo foi confirmada 1:1. Todos os arquivos são verticais `720x1280`, `24 fps`, codec de vídeo H.264, áudio AAC estéreo a `48 kHz` e apresentam rendering fotorrealista compatível com `Photorealistic / Warm Cinematic Realism`.

A tentativa de executar o rename físico no Google Drive foi iniciada, mas o conector do Drive ficou indisponível no momento da primeira escrita. Portanto, os nomes canônicos abaixo estão **confirmados como destino**, porém o rename físico no Drive ainda não foi concluído.

## Nomenclatura canônica

Para vídeos individuais de apresentação de personagem:

`VID-CHAR-XXX-APRESENTACAO-VNN.ext`

A primeira versão aprovada desta rodada usa `V01` no asset de vídeo, independentemente de a MASTER visual usada na geração ser `V02 PHOTOREALISTIC`.

## Correspondência confirmada

| Personagem | Arquivo atual no Drive | Drive file ID | Teste aprovado | Nome canônico destino | Duração | Tamanho (bytes) | SHA-256 |
| --- | --- | --- | --- | --- | ---: | ---: | --- |
| Marcos Silva (`CHAR-001`) | `Man_speaking_in_home_202608281910.mp4` | `1uN-1pXwo6SYyKdyFYOYe2F0iGk6jeti0` | `TESTE-VIDEO-MARCOS-CHAR-001-002.md` | `VID-CHAR-001-APRESENTACAO-V01.mp4` | `8.000 s` | `1,922,682` | `8ce3953a29843465b3d69c5d42305b97fa9f27bf2cb8cbec48cab70ae28d47c7` |
| Dona Célia (`CHAR-002`) | `Woman_speaking_in_home_202608281910.mp4` | `1tyDGmaWmdut_3D_ucC41vvG0XlVNtXPV` | `TESTE-VIDEO-DONA-CELIA-CHAR-002-002.md` | `VID-CHAR-002-APRESENTACAO-V01.mp4` | `8.000 s` | `4,969,732` | `2b36ab36a4900895a8ff8d442e2e88befe84751fea14c1882458fc7fb32e857a` |
| Patrícia Silva (`CHAR-003`) | `Woman_speaking_to_camera_202608281910.mp4` | `1MNr5rz6ZfwZ913bKn3IG3jld7325X5q7` | `TESTE-VIDEO-PATRICIA-CHAR-003-002.md` | `VID-CHAR-003-APRESENTACAO-V01.mp4` | `10.005 s` | `6,030,822` | `3a6bc090e33b863d3ef072d6ff65fd586cb5933aa54ae2777b5561fc62507853` |
| Sr. Antônio (`CHAR-004`) | `Antônio_speaking_in_Brazilian_home_202608281910.mp4` | `18lHr2xgBKWgFjiUqXe0pvato2ekQit9G` | `TESTE-VIDEO-ANTONIO-CHAR-004-002.md` | `VID-CHAR-004-APRESENTACAO-V01.mp4` | `8.000 s` | `7,238,697` | `ad4859381878d051a3fb55ac1fd764e8fbec79ef31eb8afd502fe602e6331fef` |
| Beto (`CHAR-005`) | `Man_speaking_to_camera_202608281910.mp4` | `1dZlsXtC7PIh-rcdqfaG_KgNuDuf1t8tw` | `TESTE-VIDEO-BETO-CHAR-005-002.md` | `VID-CHAR-005-APRESENTACAO-V01.mp4` | `10.005 s` | `3,382,289` | `dd978237499b5cb9b5dd40f3a0e56d9d5f89fecc7225e7f2708759bce4072f8b` |
| Carol Silva (`CHAR-006`) | `Carol_speaking_to_the_camera_202608281910.mp4` | `1t1SlcjIhchcO14BlDPpQC77ehbyoc1QD` | `TESTE-VIDEO-CAROL-CHAR-006-002.md` | `VID-CHAR-006-APRESENTACAO-V01.mp4` | `10.005 s` | `4,647,318` | `20309cca9f7768f43854157e0dab7ceea957d84fb4a8194eaae5b35d3a3c3c65` |
| Dudu Silva (`CHAR-007`) | `Man_speaking_Portuguese_indoors_202608281910.mp4` | `1DPdLDGgr4DAf4zBfOkuIWB0lhNAQpHDE` | `TESTE-VIDEO-DUDU-CHAR-007-001.md` | `VID-CHAR-007-APRESENTACAO-V01.mp4` | `8.000 s` | `2,577,583` | `2adc68fe1e663194e1463db75e177c2534ec02a995c156f4ae39f445aeb9be2e` |

## Critério usado para confirmação

Para cada arquivo foi confirmado:

1. personagem visível compatível com a MASTER V02 PHOTOREALISTIC correspondente;
2. vídeo individual de apresentação, e não clipe do episódio;
3. rendering `Photorealistic / Warm Cinematic Realism` consistente com o registro do teste;
4. formato vertical de produção (`720x1280`, `24 fps`);
5. áudio presente em todos os sete arquivos;
6. metadata básica e SHA-256 do binário auditado.

## Pendência remanescente

Executar apenas o rename físico no Google Drive, preservando os mesmos sete file IDs:

- `1uN-1pXwo6SYyKdyFYOYe2F0iGk6jeti0` → `VID-CHAR-001-APRESENTACAO-V01.mp4`
- `1tyDGmaWmdut_3D_ucC41vvG0XlVNtXPV` → `VID-CHAR-002-APRESENTACAO-V01.mp4`
- `1MNr5rz6ZfwZ913bKn3IG3jld7325X5q7` → `VID-CHAR-003-APRESENTACAO-V01.mp4`
- `18lHr2xgBKWgFjiUqXe0pvato2ekQit9G` → `VID-CHAR-004-APRESENTACAO-V01.mp4`
- `1dZlsXtC7PIh-rcdqfaG_KgNuDuf1t8tw` → `VID-CHAR-005-APRESENTACAO-V01.mp4`
- `1t1SlcjIhchcO14BlDPpQC77ehbyoc1QD` → `VID-CHAR-006-APRESENTACAO-V01.mp4`
- `1DPdLDGgr4DAf4zBfOkuIWB0lhNAQpHDE` → `VID-CHAR-007-APRESENTACAO-V01.mp4`

Após o rename, basta verificar os nomes por readback; os hashes não devem mudar porque o conteúdo binário será preservado.
