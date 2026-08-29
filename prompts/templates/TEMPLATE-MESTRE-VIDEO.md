# Template Mestre de Vídeo

**Status:** `FONTE OFICIAL`

Usar este arquivo para todo novo prompt de vídeo da Família Silva, principalmente no Google Flow/Veo e, quando aplicável, em outros geradores de vídeo compatíveis com as mesmas continuidades. O prompt final deve ser autossuficiente: não pode depender de memória da ferramenta, de geração anterior ou de uma referência que não esteja anexada na execução atual.

Preencher somente com informação aprovada. Se um campo obrigatório não tiver fonte, registrar `A DEFINIR` e não inventar. Blocos sem aplicação real podem ser omitidos — **exceto o conteúdo de `FICTIONAL CONTEXT DECLARATION`, quando necessário, e o de `SERIES RENDERING STYLE CONTINUITY`, que é obrigatório em todo prompt de vídeo e nunca pode ser omitido, esvaziado ou enfraquecido.**

## Regra central

**Documentation may be detailed. The final generation prompt must be concise.**

Este documento tem duas camadas:

1. **Estrutura interna de raciocínio e validação** — blocos nomeados, checklist e erros conhecidos. Servem para a IA pensar, validar e registrar a geração. **Nunca são copiados literalmente para a ferramenta.**
2. **Prompt final** — o texto efetivamente colado no gerador. Deve ser **prosa natural, enxuta, sem cabeçalhos técnicos, sem campos `A DEFINIR`, sem IDs e sem estrutura administrativa.**

### Disciplina de evidência

Aplicar a sequência aprovada em [DEC-019](../../docs/DECISOES.md#dec-019):

`HIPÓTESE → EM TESTE → VALIDADO → decisão/template`

Não promover um comportamento de ferramenta a regra permanente com base apenas em uma primeira impressão ou em um único resultado cuja causa/mecanismo ainda seja ambíguo.

Exemplo importante de `2026-08-29`: existe um arquivo final de S01E001 auditado com `20.010 s`, mas o binário **não prova por si só** se sua origem foi geração única, extensão, continuação ou sequência na interface do Gemini. O benefício narrativo do multi-beat foi validado; a hipótese de “20s diretos em toda geração” não foi.

Antes de segmentar um roteiro, aplicar [LRN-015](../../docs/APRENDIZADOS-DE-VIDEO.md#lrn-015--arquitetura-narrativa-multi-beat-para-microcenas-encadeadas): microcenas causal ou emocionalmente conectadas podem ser avaliadas como beats de uma sequência contínua **se a ferramenta, a duração real e a complexidade permitirem**. Isso complementa, e não revoga, a arquitetura de microclipes.

## Metadados do registro

- **Prompt ID:** `PROMPT-CHAR-XXX-VIDEO-XXX`
- **Versão:** `VXX`
- **Status:** `EM TESTE`
- **Ferramenta/modelo:** `A DEFINIR`
- **Personagem(ns):** `A DEFINIR`
- **Cena/episódio:** `A DEFINIR`
- **Arquitetura:** `MICROCLIPE`, `MULTI-BEAT` ou `CONTINUAÇÃO/EXTENSÃO` quando comprovadamente usada
- **Referências anexadas nesta geração:** `A DEFINIR`
- **Ordem real dos anexos:** `A DEFINIR` quando houver múltiplas referências
- **Duração/configuração real selecionada na ferramenta:** `A DEFINIR`

## Estrutura interna de raciocínio e validação (NÃO é o prompt final)

```text
FICTIONAL CONTEXT DECLARATION
This video belongs to Família Silva, an original fictional Brazilian family comedy. Every named character is an original fictional character. Use only the project-owned reference images attached to this generation.

SCENE OBJECTIVE
[State the exact purpose of this shot or sequence.]

NARRATIVE ARCHITECTURE
[Choose MICROCLIP, MULTI-BEAT, or CONTINUATION/EXTENSION only when that workflow is actually being used.]
[If MULTI-BEAT, list the beats in chronological order and explain the causal/emotional connection.]
[Do not assume a duration or generation mechanism from a previous output.]
[Use MICROCLIP when platform limits, dialogue length, visual drift, scene complexity or speaking/lip-sync risk make the longer sequence unreliable.]

CHARACTERS PRESENT
[List only the characters who must be visible, by name and approved role.]
[Character IDs remain in metadata, never in the final prompt.]
[For MULTI-BEAT, state which characters are present in each beat if the cast changes.]

CURRENT GENERATION REFERENCES
[List every attached reference and the character it belongs to. Use each character's current canonical MASTER V02 PHOTOREALISTIC unless a specific approved source requires otherwise.]
Use the uploaded master images as visual references and preserve the established appearance of each character consistently.
Each character must use only their own approved reference.

REFERENCE COMPLETENESS CHECK
[Every character named in the reference sentence has their own MASTER attached: YES/NO.]
[No required MASTER is missing: YES/NO.]

REFERENCE ORDER CHECK — GEMINI MULTI-REFERENCE
[When using Gemini with multiple character references, record the names in the exact order they appear in the prompt and verify that the uploaded images follow the same 1:1 order.]
[Example: Carol, Marcos, Patrícia, Dudu → upload Carol MASTER, Marcos MASTER, Patrícia MASTER, Dudu MASTER.]
[This ordering rule is validated for Gemini in the 2026-08-29 production round; do not generalize automatically to other tools without equivalent evidence.]

CHARACTER VISUAL CONTINUITY
For each visible character, preserve the approved facial features, apparent age, hair, body build, height, proportions, silhouette, and distinguishing visual features shown in that character's own attached MASTER V02 PHOTOREALISTIC.
Maintain stable facial structure, body build, weight, anatomy, skin texture, hair, and proportions from first frame to last.
No facial drift, body drift, weight change, age change, morphing, feature blending, or character mixing.

SERIES RENDERING STYLE CONTINUITY
Photorealistic / Warm Cinematic Realism. Mandatory in every prompt: "Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment."
Use physically plausible materials, realistic depth of field, and grounded color.
Avoid flat cartoon rendering, childlike animation, toy-like appearance, waxy or plastic skin, exaggerated proportions, and visual imitation of any named studio, franchise, artwork, or artist.

COSTUME CONTINUITY
[Describe only approved costume information needed for the scene.]
Keep garments, colors, fabrics, accessories, footwear, fit and state of wear stable inside the same temporal block.
No spontaneous wardrobe or accessory changes.

ENVIRONMENT CONTINUITY
[Describe the approved location, layout, permanent objects, lighting and time of day needed for this generation.]
Keep architecture, furniture, props, object placement, colors and lighting direction stable.
[For MULTI-BEAT, describe a simple narratively justified transition; do not invent a large jump merely to fill duration.]

SHOT, CAMERA, AND COMPOSITION
Format: [for example, vertical 9:16].
Framing: [A DEFINIR].
Camera position and movement: [A DEFINIR].
Lens and depth of field: [A DEFINIR].
Composition: [A DEFINIR].
Do not introduce unrequested characters, objects, text, logos or arbitrary camera moves.

ACTION AND PERFORMANCE
[Describe the action in chronological order.]
[Describe expression, posture, gestures, reactions and comedic/emotional timing.]
[For MULTI-BEAT, explain how the emotional state entering each beat is changed by the preceding beat.]
Keep movement natural, physically plausible, restrained and consistent with canonical personality.

EMOTIONAL PERFORMANCE AND ORALITY
[State the specific emotion: urgency, frustration, embarrassment, regret, affection, irony, resignation, etc.]
Dialogue must sound spoken, not written. Natural Brazilian oral rhythm may include brief repetitions, interjections, hesitations and pauses when character-appropriate.
Do not force theatrical melodrama. Emotion should remain grounded and believable.

RELATIONSHIP CONTINUITY
[State only the approved relationship and interaction dynamic necessary for the scene.]
Do not infer a new relationship.

DIALOGUE MAP
[For MICROCLIP:]
Speaker: [Character name]
Exact dialogue in Brazilian Portuguese: "[LITERAL DIALOGUE]"
Silent characters: [names]

[For MULTI-BEAT:]
Beat 1 — Speaker: [Character name]
Exact dialogue: "[LITERAL DIALOGUE]"
Beat 1 — Silent characters: [names]

Beat 2 — Speaker: [Character name]
Exact dialogue: "[LITERAL DIALOGUE]"
Beat 2 — Silent characters: [names]

[Repeat only as needed.]

DIALOGUE DURATION FIT
[Does the line fit the real configured duration while preserving pauses, emotion and reactions? YES/NO.]
[If NO, shorten the line before generation. Do not rely on artificially fast delivery.]

SPEAKING AND VOICE
Only the assigned speaker for the current beat speaks. Everyone else visible in that beat remains silent. Each line belongs only to its assigned speaker — never exchange, blend, redistribute, complete or add dialogue.

LIP-SYNC
Only the speaking character in the current beat shows lip movement matching the exact Portuguese dialogue. Silent characters may react through expression, eye movement, posture and gesture, but do not mouth words.

AUDIO
Dialogue: clear Brazilian Portuguese, foreground and intelligible.
Ambience: [A DEFINIR].
Music: [A DEFINIR or none].
Sound effects: [A DEFINIR or none].
No extra voices or narration unless specifically approved.

NEGATIVE CONSTRAINTS
[Keep this list short and case-specific. Do not duplicate every positive continuity rule.]

OUTPUT CLEANLINESS
No subtitles, captions, on-screen text, logos, watermarks, visible Character IDs or administrative scene/clip labels.

TECHNICAL OUTPUT
Duration/configuration: [record the value actually selected in the tool].
Aspect ratio: [A DEFINIR].
Resolution: [A DEFINIR].
Frame rate: [A DEFINIR].
Number of shots/beats: [A DEFINIR].
Audio enabled: [A DEFINIR].
Generation quantity: [A DEFINIR].
[Do not infer the mechanism of generation solely from final file duration.]

FINAL CONTINUITY CHECK
Generate only the described original fictional scene. Preserve every supplied approved reference and dialogue assignment. When an instruction is not defined, do not invent a new canonical trait, relationship, costume, voice, prop or location.
```

## Do raciocínio interno ao prompt final

Depois de preencher a estrutura acima, reescreva como prosa natural em inglês. Regras obrigatórias:

**A. Live-action explícito.** Todo prompt final deve conter, quase literalmente: `Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment.`

**B. Sem cabeçalhos administrativos.** Remover rótulos internos como `SCENE OBJECTIVE`, `CHARACTERS PRESENT`, `TECHNICAL OUTPUT`, `REFERENCE ORDER CHECK` etc.

**C. Omitir campos não definidos.** Nunca escrever `A DEFINIR` no prompt final. Se algo não é necessário, omitir.

**D. Locks em frases naturais.** Em microclipe: `Only [NAME] speaks. Everyone else remains silent.` Em multi-beat, declarar a exclusividade por beat.

**E. Fictional context com moderação.** Não repetir automaticamente linguagem longa sobre pessoas reais; usar contexto adicional apenas quando necessário para compliance.

**F. Referência MASTER concisa.** Usar wording como: `Use the uploaded master images of [NAMES] as visual references and preserve their established appearance consistently.` Anexar todas as MASTERs V02 necessárias. **No Gemini multi-reference, a ordem de upload deve acompanhar a ordem dos nomes no prompt, conforme LRN-017/DEC-019.**

**G. Fala emocional e oral.** O texto deve soar como fala real em PT-BR. Permitir pequenas interjeições, repetições e pausas quando melhorarem naturalidade. A fala precisa caber na duração real com atuação, não somente na leitura acelerada.

**H. Regra central.** Documentation may be detailed. The final generation prompt must be concise.

## Arquitetura narrativa multi-beat

O princípio multi-beat é **narrativo e condicional**. Antes de agrupar, verificar:

1. O segundo beat é consequência, continuação ou transformação direta do primeiro?
2. Ambiente, faixa temporal e figurino são compatíveis?
3. Elenco e fala permanecem controláveis?
4. A duração/configuração realmente disponível na ferramenta comporta os beats e suas falas?
5. O método real será geração única, extensão/continuação ou outra operação? Se não estiver comprovado, não inventar a resposta no registro.

Se for seguro, o prompt pode usar arquitetura equivalente a:

```text
Create one continuous vertical 9:16 sequence with two connected dramatic-comedic beats, keeping smooth continuity of character appearance, costume, environment and emotional progression.

First beat: [action, emotion, exact dialogue, speaker, silent characters].

Then continue naturally into the second beat: [consequence, emotion, exact dialogue, speaker, silent characters].

The emotional progression must be clear: [how beat 1 causes or transforms beat 2].
```

Esse exemplo é de arquitetura, não texto fixo e não implica `20s`.

### Quando NÃO agrupar

Voltar a microclipes quando houver:

- duração insuficiente para as falas e reações;
- mudança grande de ambiente, horário ou figurino;
- elenco ou ações simultâneas demais;
- diálogo sobreposto ou alto risco de troca de fala, voz ou lip sync;
- deriva visual/narrativa;
- plataforma/configuração incompatível;
- resultado empiricamente pior que a versão curta.

## Baseline opcional para teste curto no Flow

Quando o objetivo for repetir a configuração historicamente validada de teste curto no Flow:

- **Fluxo:** `Vídeo → Elementos`.
- **Referências:** adicionadas como Elementos.
- **Modelo:** `Veo 3.1 Lite`.
- **Proporção:** `9:16`.
- **Quantidade:** `x1`.
- **Duração:** `8s`.

Essa baseline não define duração da série e não deve ser extrapolada para o Gemini ou outros fluxos.

## Gemini — múltiplas referências

Aprendizado validado em `2026-08-29` ([ERR-009](../../producao/erros/ERR-009-GEMINI-MASTERS-AUSENTES-OU-FORA-DE-ORDEM.md) / [SOL-009](../../producao/solucoes/SOL-009-GEMINI-MASTERS-COMPLETAS-E-ORDENADAS.md)):

1. anexar todas as MASTERs citadas;
2. verificar que não falta referência de nenhum personagem;
3. manter a mesma ordem entre a frase de referências e os arquivos anexados;
4. conferir o pareamento 1:1 antes de gerar.

Exemplo:

`Use the uploaded master images of Carol, Marcos, Patrícia and Dudu...`

Upload: `Carol → Marcos → Patrícia → Dudu`.

Essa ordem é regra operacional do Gemini nesta rodada, não regra universal de toda ferramenta.

## Bloqueios e erros — como corrigir sem sacrificar o realismo

- **Cartoon/plástico:** reforçar `Photorealistic / Warm Cinematic Realism`; não recorrer a estúdio/franquia como atalho.
- **Fala/voz/lip-sync trocados:** reduzir falantes concorrentes e explicitar speaker/silêncio por beat.
- **IDs/texto aparecendo:** remover Character IDs, labels administrativos e duração escrita como narrativa.
- **Prompt rígido demais:** aplicar simplificação controlada.
- **Falso positivo de pessoa famosa:** usar apenas o fallback ficcional validado, sem enfraquecer live-action.
- **Gemini retorna erro genérico:** antes de reescrever a cena, conferir se todas as MASTERs pedidas foram anexadas e se o conjunto está correto. Nem todo erro genérico tem essa causa, mas foi a causa validada em ERR-009.
- **Personagens/falas invertidos no Gemini multi-reference:** conferir a ordem dos anexos versus a ordem dos nomes.
- **Fala cortada:** reduzir o texto considerando pausa, emoção e reação antes de regenerar.

## Registro pós-geração

Após gerar, registrar:

- ferramenta/modelo;
- arquitetura realmente usada;
- prompt ID/versão;
- referências realmente fornecidas;
- ordem real das referências quando relevante;
- duração/configuração realmente selecionada;
- duração e metadata do arquivo final quando disponíveis;
- resultado observado;
- erros factuais;
- hipóteses separadas dos fatos;
- solução testada;
- dimensão aprovada;
- impacto no cânone/produção.

## Checklist antes de entregar qualquer prompt

- [ ] O prompt final está em prosa natural, sem cabeçalhos administrativos?
- [ ] Não contém `A DEFINIR`, Character IDs ou labels técnicos?
- [ ] É explicitamente live-action e photorealistic?
- [ ] Segue `Photorealistic / Warm Cinematic Realism`?
- [ ] Todas as MASTERs necessárias estão anexadas?
- [ ] Cada personagem usa sua própria MASTER V02?
- [ ] No Gemini multi-reference, a ordem dos anexos acompanha a ordem dos nomes no prompt?
- [ ] A fala está atribuída ao personagem correto?
- [ ] Personagens silenciosos permanecem silenciosos e não executam lip sync?
- [ ] As falas estão em PT-BR e as instruções em inglês?
- [ ] O diálogo soa falado, natural e emocionalmente específico?
- [ ] A fala cabe na duração real com pausas e reações?
- [ ] Se multi-beat, há relação causal/emocional clara?
- [ ] Se a duração/configuração não comporta os beats, o prompt foi revertido para microclipes ou uma continuação realmente suportada?
- [ ] Não há texto, legenda, logo ou marca d'água na tela?
- [ ] Character/Costume/Environment/Relationship Continuity estão respeitadas?
- [ ] Negative Constraints são curtas e específicas?
- [ ] Qualquer afirmação nova sobre comportamento da ferramenta está marcada como hipótese/teste até validação suficiente?
- [ ] O prompt foi comparado com [APRENDIZADOS-DE-VIDEO.md](../../docs/APRENDIZADOS-DE-VIDEO.md) e [APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md](../../docs/APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md)?

## Reference Examples — illustrative, not production-verified

Os exemplos abaixo ilustram formato. Não devem ser apresentados como transcrição histórica de um prompt aprovado se a fonte literal não estiver registrada.

### Exemplo 1 — Personagem único

```text
Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment. Use the uploaded master image of Marcos as the visual reference and preserve his established appearance consistently.

Marcos is alone, facing the camera directly in a medium shot. He speaks warmly and naturally, with relaxed body language.

Only Marcos speaks. No other voices are heard. His lips match his exact dialogue in Brazilian Portuguese: "[EXACT LINE]"

No subtitles, captions, logos, or on-screen text.
```

### Exemplo 2 — Dois personagens, um falante

```text
Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment. Use the uploaded master images of Carol and Beto as visual references and preserve their established appearances consistently.

Carol and Beto stand together in the kitchen. Carol delivers her line naturally. Beto reacts but stays silent.

Only Carol speaks. Beto remains silent. Carol says in Brazilian Portuguese: "[EXACT LINE]"

No subtitles, captions, logos, or on-screen text.
```

### Exemplo 3 — Dois beats conectados

```text
Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment. Use the uploaded master images of the visible characters as visual references and preserve their established appearances consistently.

Create a continuous sequence with two connected dramatic-comedic beats, keeping smooth continuity of character appearance, costume, environment and emotional progression.

First beat: [event]. [NAME] says in Brazilian Portuguese: "[EXACT LINE]" Only [NAME] speaks. Everyone else remains silent and reacts naturally.

Then continue naturally into the second beat as a direct consequence: [event]. [SECOND NAME] says in Brazilian Portuguese: "[EXACT LINE]" Only [SECOND NAME] speaks. Everyone else remains silent.

Keep performances grounded and believable. No subtitles, captions, logos or visible text.
```

## Erros conhecidos e como evitar regressões

1. **Cartoon / desenho / plástico** — `ERR-001`: usar rendering canônico explícito.
2. **Deriva visual corporal** — `ERR-002`: reforçar continuidade física da própria MASTER.
3. **Fala, voz ou lip sync trocados** — `ERR-003`: speaker/silêncio explícitos por beat.
4. **Prompt dependente de contexto anterior** — `ERR-004`: prompt autossuficiente e referências atuais anexadas.
5. **Referência facial cruzada** — `ERR-005`: cada personagem usa exclusivamente a própria MASTER.
6. **Referência não neutra** — `ERR-006`: evitar elementos indesejados na imagem de referência.
7. **Texto/ID/rótulo técnico aparecendo** — `ERR-007`: remover labels administrativos e wording excessivamente rígido.
8. **Falso positivo de pessoa famosa** — `ERR-008`: usar fallback ficcional somente quando necessário.
9. **Gemini com MASTERs ausentes ou fora de ordem** — [ERR-009](../../producao/erros/ERR-009-GEMINI-MASTERS-AUSENTES-OU-FORA-DE-ORDEM.md): anexar o conjunto completo e alinhar a ordem no Gemini.
10. **Vídeo complexo demais para a duração** — risco validado em S01E001: reduzir fala/ações ou dividir beats; não aceitar corte de diálogo apenas para manter agrupamento.
11. **Hipótese promovida cedo demais** — aprendizado de `2026-08-29`: separar fato observado de interpretação e aplicar `HIPÓTESE → EM TESTE → VALIDADO → decisão/template`.
