# Aprovação — música-tema Família Silva — 001

- **Status:** `APROVADO / CURRENT CANON — MASTER`
- **Data:** `2026-08-29`
- **Asset:** `ASSET-SERIES-002`
- **Arquivo:** [AUD-FAMILIA-SILVA-TEMA-V01.wav](../../assets/audio/tema/AUD-FAMILIA-SILVA-TEMA-V01.wav)
- **Versão:** `V01`
- **Ferramenta:** Google Flow Music (geração musical). **Não** é o Google Flow de vídeo.
- **Prompt/direção exata usada na geração:** `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` — não recuperada nesta tarefa; apenas o conceito musical (abaixo) foi registrado.
- **Decisão:** [DEC-021](../../docs/DECISOES.md#dec-021).
- **Manifesto do asset:** [assets/audio/README.md](../../assets/audio/README.md).
- **Registro da sessão:** [TESTE-AUDIO-MUSICA-TEMA-SERIE-001.md](../testes/TESTE-AUDIO-MUSICA-TEMA-SERIE-001.md).

## Dimensão aprovada

Identidade musical da série Família Silva (música-tema oficial). A aprovação cobre a faixa como um todo: composição, arranjo, andamento, mixagem e interpretação vocal genérica presentes no arquivo aprovado.

A aprovação **não** cobre:

- voz canônica de qualquer personagem (Marcos, Patrícia ou outro) — permanece `A DEFINIR`;
- letra longa inicial como texto executado integralmente;
- uso obrigatório em todos os episódios ou duração de trilha por episódio;
- logo sonoro, vinheta curta derivada, versão instrumental ou remixes — cada um seria nova versão com nova validação.

## Evidência de aprovação

A música foi criada e refinada numa sessão de experimentação no Google Flow Music em `2026-08-29`. O usuário ouviu as versões produzidas e aprovou explicitamente a versão final, declarando que gostou dela e que não deseja continuar buscando aperfeiçoamentos. Princípio declarado na aprovação: o objetivo não é perseguir perfeição indefinidamente; a faixa aprovada já cumpre satisfatoriamente sua função de identidade musical da Família Silva. A decisão é final para o estado atual do projeto.

## Validação técnica realizada

Arquivo auditado localmente antes do registro (`ffprobe`, `sha256sum`, `cmp`):

- Container/codec: WAV / PCM signed 16-bit little-endian (`pcm_s16le`).
- Sample rate: `48000 Hz`.
- Canais: `2` (estéreo).
- Profundidade: `16-bit`.
- Duração: `177.258667 s` (~2 min 57 s). Apesar do nome experimental "Title Card Sting", **não** é um sting curto.
- Tamanho: `34046710` bytes.
- Bitrate: `1536 kbps`.
- Tag de encoder do export: `Lavf59.27.100`.
- SHA-256: `6dcd5d835258d6d67c0ab81b7eadfb2db003c8aef9b83a955c69cbfac478d30f`.
- O arquivo no repositório é cópia byte a byte do arquivo experimental de origem (`cmp` sem diferença; mesmo SHA-256). Sem reencode, recompressão ou alteração sonora.
- `Família Silva - Title Card Sting (1).wav` (origem) é byte a byte idêntico e não é versão distinta.

## Conceito musical (contexto de produção)

- música-tema original para sitcom/comédia familiar brasileira;
- samba-pop brasileiro contemporâneo; influência leve de pagode-pop; elementos de MPB contemporânea;
- instrumentação orgânica; clima brasileiro, caloroso, familiar, alegre e brincalhão;
- humor a partir da identidade da família e da letra, sem estética infantil nem de paródia;
- soar como músicos reais, não como jingle publicitário;
- voz principal masculina adulta brasileira; backing vocals masculinos e femininos no refrão;
- intérpretes neutros — nenhum personagem canônico é o cantor.

## Letra

- Hook aprovado: `"Família Silva, é assim"`.
- A primeira letra planejada (apresentação individual de personagens) foi parcialmente omitida/reorganizada pelo Flow Music nos testes. Uma V02 mais curta concentrou-se no universo familiar e no hook. O usuário aceitou que a versão final não executa literalmente toda a letra longa inicial.
- Transcrição literal da faixa aprovada: `PENDENTE` (sem ferramenta de transcrição confiável nesta tarefa). Não reconstruir por suposição.

## Versões anteriores

As seis faixas anteriores da sessão permanecem `EXPERIMENTAL / HISTÓRICO` (não `REJEITADO`). Catalogadas com SHA-256 e duração em [assets/audio/README.md](../../assets/audio/README.md). Binários não versionados por tamanho; preservados na origem `C:\Users\vanze\OneDrive\Documentos\Downloads\`.

## Limites

- A aprovação não promove nenhuma voz da faixa a Voice Master de personagem.
- A aprovação não abrange logo, capa, banner, thumbnail, campanha de lançamento ou estratégia de uso da música nas redes.
- Qualquer nova geração, corte, versão instrumental ou remix constitui nova versão e exige nova validação.
