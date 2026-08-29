# Áudio

Este diretório guarda a identidade sonora aprovada da série Família Silva e as referências sonoras em avaliação.

Assets experimentais não são cânone. Apenas arquivos versionados, identificados e vinculados a uma decisão formal podem ser tratados como MASTER.

## Subdiretórios

- [tema/](tema/) — música-tema oficial da série.

## Asset vigente — MASTER

| Asset ID | Arquivo | Versão | Status | Formato | Sample rate | Canais | Profundidade | Duração | SHA-256 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `ASSET-SERIES-002` | [tema/AUD-FAMILIA-SILVA-TEMA-V01.wav](tema/AUD-FAMILIA-SILVA-TEMA-V01.wav) | `V01` | `CURRENT CANON / MASTER` | WAV PCM `s16le` | `48000 Hz` | `2` (estéreo) | `16-bit` | `177.258667 s` (~2 min 57 s) | `6dcd5d835258d6d67c0ab81b7eadfb2db003c8aef9b83a955c69cbfac478d30f` |

- **Título:** Tema da Família Silva (música-tema oficial da série).
- **Finalidade:** identidade musical da série; uso previsto em abertura/encerramento e vinhetas dos episódios (ver [FONTE-HISTORICA-S01E001](../../episodios/S01/FONTE-HISTORICA-S01E001-A-GREVE-DA-PATRICIA.md), seção 7 — montagem).
- **Origem:** Google Flow Music (ferramenta de geração musical). Tag de encoder do export: `Lavf59.27.100`.
- **Data de criação/refinamento:** `2026-08-29`.
- **Data de aprovação:** `2026-08-29`.
- **Tamanho:** `34046710` bytes.
- **Bitrate:** `1536 kbps` (PCM não comprimido).
- **Arquivo experimental de origem:** `Família Silva - Title Card Sting.wav` (nome experimental da sessão; ver correspondência abaixo).
- **Decisão:** [DEC-021](../../docs/DECISOES.md#dec-021).
- **Registro de aprovação:** [APROVACAO-MUSICA-TEMA-FAMILIA-SILVA-001](../../producao/aprovados/APROVACAO-MUSICA-TEMA-FAMILIA-SILVA-001.md).
- **Registro da sessão de criação:** [TESTE-AUDIO-MUSICA-TEMA-SERIE-001](../../producao/testes/TESTE-AUDIO-MUSICA-TEMA-SERIE-001.md).

### Correspondência arquivo experimental → arquivo oficial

| Arquivo experimental original | Arquivo oficial no repositório |
| --- | --- |
| `Família Silva - Title Card Sting.wav` | `AUD-FAMILIA-SILVA-TEMA-V01.wav` |

O nome experimental continha "Title Card Sting", mas esta é a faixa completa (~2 min 57 s) que o usuário escolheu manter como a música oficial da série. O nome experimental **não** foi preservado como nome MASTER; a renomeação foi cópia byte a byte, sem reencode, recompressão ou alteração sonora (SHA-256 idêntico ao arquivo de origem).

Uma cópia adicional baixada, `Família Silva - Title Card Sting (1).wav`, é byte a byte idêntica ao arquivo aprovado (mesmo SHA-256) e não constitui uma versão distinta.

## Conceito musical desenvolvido na sessão

Direção usada durante a criação, registrada como contexto de produção (não como regra canônica geral):

- música-tema original para sitcom/comédia familiar brasileira;
- samba-pop brasileiro contemporâneo, com influência leve de pagode-pop e elementos de MPB contemporânea;
- instrumentação orgânica; clima brasileiro, caloroso, familiar, alegre e brincalhão;
- humor vindo da identidade da família e da letra, sem estética infantil nem de paródia;
- intenção de soar como músicos reais, evitando estética de jingle publicitário;
- voz principal masculina adulta brasileira; backing vocals masculinos e femininos no refrão;
- intérpretes neutros: a faixa **não** estabelece que qualquer personagem canônico esteja cantando.

## Letra — o que está confirmado e o que não está

- **Conceito/hook aprovado:** `"Família Silva, é assim"`.
- **Processo:** a primeira letra planejada apresentava individualmente vários personagens; nos testes o Google Flow Music omitiu/reorganizou partes. Uma V02 mais curta foi criada, concentrada no universo familiar e no hook. O usuário aceitou conscientemente que a versão final não precisava executar literalmente toda a letra longa inicial.
- **NÃO registrar** a primeira letra longa como "letra oficial executada integralmente" — isso não corresponde ao áudio final.
- **Transcrição literal da faixa aprovada:** `PENDENTE` — não foi feita nesta tarefa por ausência de ferramenta de transcrição confiável. Não inventar transcrição do WAV.

## Histórico da sessão — versões experimentais (NÃO são MASTER)

Produzidas na mesma sessão do Google Flow Music em `2026-08-29`. Status: `EXPERIMENTAL / HISTÓRICO` — não `REJEITADO`. Somente a última faixa foi explicitamente aprovada como música oficial.

Os binários experimentais **não foram versionados neste repositório** (cada arquivo tem ~30–35 MB; sete arquivos). Ficam preservados na origem: `C:\Users\vanze\OneDrive\Documentos\Downloads\`. Metadados verificados por `ffprobe` e `sha256sum`:

| Ordem | Arquivo experimental | Duração | SHA-256 | Observação |
| --- | --- | --- | --- | --- |
| 1 | `Família Silva.wav` | `167.264000 s` | `ed9fe5e6e590184d29a50572cd8ed6919140a258e029b61566795f31651f353b` | 1ª geração; letra longa de apresentação de personagens |
| 2 | `Família Silva (1).wav` | `168.661333 s` | `3b67607e528a716762bfa8e34fecd730c04a1000577260af6714d99b09c13f42` | variação da 1ª geração |
| 3 | `Família Silva (V02).wav` | `156.778667 s` | `d6ebf178c07e0742650fb6c5a3477aa4eb582c54faaceea5868eaf462b94e779` | V02 mais curta; foco no universo familiar e no hook |
| 4 | `Família Silva (V02) (1).wav` | `163.189333 s` | `a84a8d9d2daefa448b3c0d68af802b131b2b0d7dc7f4ee071f62b419d2528255` | variação da V02 |
| 5 | `Família Silva - Hook Experiment A.wav` | `180.821333 s` | `0c140da20e48d33761b9270c33339312579f7f44b63295d9d4f2489efaef2c1b` | teste específico de hook (A) |
| 6 | `Família Silva - Hook Experiment B.wav` | `177.258667 s` | `e9b2d02e7075eab15a01007ebf01d8e13746cbd378b2e2ad2720ec80c53ed16b` | teste específico de hook (B) |
| 7 | `Família Silva - Title Card Sting.wav` | `177.258667 s` | `6dcd5d835258d6d67c0ab81b7eadfb2db003c8aef9b83a955c69cbfac478d30f` | **APROVADA — promovida a `ASSET-SERIES-002` / `AUD-FAMILIA-SILVA-TEMA-V01.wav`** |

Todos os arquivos acima: WAV PCM `s16le`, `48000 Hz`, `2` canais, `16-bit`.

## Limite de cânone

- Esta faixa é a identidade musical da série. Ela **não** define, aprova nem sugere a voz canônica de Marcos, Patrícia ou de qualquer personagem. Vozes individuais permanecem `A DEFINIR` até aprovação específica (ver [docs/CONTINUIDADE.md](../../docs/CONTINUIDADE.md) e [producao/STATUS.md](../../producao/STATUS.md)).
- Nenhuma personalidade, relação ou decisão visual/narrativa é alterada por este asset.
- Novas versões devem receber numeração própria (`V02`, `V03` etc.) e nova aprovação explícita. A faixa aprovada não deve ser reencodada nem recomprimida no processo de organização.

## Promoção de novo áudio a MASTER

1. Adicionar o arquivo correto.
2. Registrar origem, finalidade, data, versão, metadados técnicos verificáveis e SHA-256.
3. Atribuir Asset ID conforme [docs/NOMENCLATURA.md](../../docs/NOMENCLATURA.md).
4. Obter aprovação explícita e registrar a decisão em [docs/DECISOES.md](../../docs/DECISOES.md).
5. Registrar a aprovação em [producao/aprovados/](../../producao/aprovados/) e atualizar changelog e status.
