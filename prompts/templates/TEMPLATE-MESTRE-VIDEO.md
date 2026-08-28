# Template Mestre de Vídeo

**Status:** `FONTE OFICIAL`

Usar este arquivo para todo novo prompt de vídeo da Família Silva, principalmente no Google Flow/Veo. O prompt final deve ser autossuficiente: não pode depender de memória da ferramenta, de geração anterior ou de uma referência que não esteja anexada na execução atual.

Preencher somente com informação aprovada. Se um campo obrigatório não tiver fonte, registrar `A DEFINIR` e não inventar. Blocos sem aplicação real podem ser omitidos.

## Metadados do registro

- **Prompt ID:** `PROMPT-CHAR-XXX-VIDEO-XXX`
- **Versão:** `VXX`
- **Status:** `EM TESTE`
- **Ferramenta/modelo:** `A DEFINIR`
- **Personagem(ns):** `A DEFINIR`
- **Cena/episódio:** `A DEFINIR`
- **Referências anexadas nesta geração:** `A DEFINIR`

## Template para copiar e preencher

```text
FICTIONAL CONTEXT DECLARATION
This video belongs to Família Silva, an original fictional Brazilian family sitcom. Every named character is an original fictional character. Use only the project-owned reference images attached to this generation. Do not interpret any character as a real person and do not imitate a real person's likeness.

SCENE OBJECTIVE
[State the exact purpose of this shot.]

CHARACTERS PRESENT
[List only the characters who must be visible, with Character ID and approved role in the scene.]
[For an individual shot, state that only the requested character is visible.]

CURRENT GENERATION REFERENCES
[List each attached reference and the character, costume, or environment it belongs to.]
[Each character must use only their own approved MASTER image or approved visual reference.]
[A prior approved video may guide only the specifically approved method or rendering dimension; it never replaces the character's own facial reference.]

CHARACTER VISUAL CONTINUITY
For each visible character, preserve the approved facial features, apparent age, hair, body build, height, proportions, silhouette, and distinguishing visual features shown in that character's own attached approved reference.
Maintain stable facial structure, body build, weight, anatomy, skin texture, hair, and proportions from the first frame to the last.
No facial drift, body drift, weight change, age change, morphing, feature blending, or character mixing.
[Add only approved character-specific details.]

SERIES RENDERING STYLE CONTINUITY
Photorealistic / Warm Cinematic Realism.
Use natural skin texture, physically plausible materials, believable human anatomy and proportions, warm cinematic lighting, realistic depth of field, grounded color, and subtle live-action-adjacent polish.
Avoid flat cartoon rendering, childlike animation, toy-like appearance, waxy or plastic skin, exaggerated proportions, and visual imitation of any named studio, franchise, artwork, or artist.

COSTUME CONTINUITY
[Describe only the approved costume attached to or documented for each character.]
Keep every garment, color, fabric, accessory, footwear item, fit, and state of wear stable for the full shot.
No spontaneous wardrobe or accessory changes.

ENVIRONMENT CONTINUITY
[Describe the approved location, layout, permanent objects, lighting, time of day, and continuity requirements.]
Keep architecture, furniture, props, object placement, colors, and lighting direction stable.

SHOT, CAMERA, AND COMPOSITION
Format: [for example, vertical 9:16].
Framing: [A DEFINIR].
Camera position and movement: [A DEFINIR].
Lens and depth of field: [A DEFINIR].
Composition: [A DEFINIR].
Do not introduce unrequested characters, objects, text, logos, cuts, or camera moves.

ACTION AND PERFORMANCE
[Describe the action in chronological order.]
[Describe approved expression, posture, gestures, reaction, and comedic timing.]
Keep movement natural, physically plausible, restrained, and consistent with the character's canonical personality.

RELATIONSHIP CONTINUITY
[For scenes with multiple characters, state only the approved relationship, distance, form of address, and interaction dynamic needed in this scene.]
Do not infer or create a new relationship.

DIALOGUE MAP
Speaker: [Character name and ID]
Exact dialogue in Brazilian Portuguese: "[LITERAL DIALOGUE]"
Voice source/status: [approved voice reference or A DEFINIR]
Speaking interval: [A DEFINIR]

[Repeat the four lines above for every speaker.]

SPEAKING CONTINUITY
Each line belongs exclusively to its assigned speaker. Never exchange, redistribute, merge, complete, paraphrase, or add dialogue. Only the assigned speaker may pronounce that line.

VOICE CONTINUITY
Keep each approved voice linked only to its assigned character. Do not exchange voices, blend voices, or create an unapproved permanent voice. If the voice is experimental, treat it as experimental and do not imply canonical approval.

LIP-SYNC CONTINUITY
Only the active speaker performs lip sync. Mouth movement must match that speaker's exact Portuguese dialogue and assigned voice. No other character may mouth, echo, or simulate the line.

SILENT CHARACTER CONTINUITY
[List every visible silent character.]
Silent characters never speak and never move their lips as if speaking. They may react naturally through approved facial expression, eye movement, posture, and gesture.

AUDIO
Dialogue: clear Brazilian Portuguese, foreground and intelligible.
Ambience: [A DEFINIR].
Music: [A DEFINIR or none].
Sound effects: [A DEFINIR or none].
No extra voices, narration, crowd speech, or unrequested vocal sounds.

NEGATIVE CONSTRAINTS
No visual drift; no facial or body morphing; no weight or age change; no character mixing; no duplicate person; no extra limbs or fingers; no deformed hands; no wardrobe mutation; no environment mutation; no unrequested character; no text or logo unless explicitly approved; no dialogue swap; no voice swap; no lip-sync assignment error; no speaking by silent characters; no flat cartoon; no plastic skin; no childlike animation; no exaggerated anatomy.
[Add case-specific restrictions supported by an approved source.]

TECHNICAL OUTPUT
Duration: [A DEFINIR].
Aspect ratio: [A DEFINIR].
Resolution: [A DEFINIR].
Frame rate: [A DEFINIR].
Number of shots: [A DEFINIR].
Audio enabled: [A DEFINIR].
Generation quantity: [A DEFINIR].

FINAL CONTINUITY CHECK
Generate only the described original fictional scene. Preserve every supplied approved reference and every dialogue assignment. When an instruction is not defined above, do not invent a new canonical character trait, relationship, costume, voice, prop, or location.
```

## Baseline opcional para teste curto no Flow

Quando o objetivo for repetir a configuração já validada de teste, preencher:

- **Fluxo:** `Vídeo → Elementos`.
- **Referências:** anexadas como Elementos, não Frames.
- **Modelo:** `Veo 3.1 Lite`.
- **Proporção:** `9:16`.
- **Quantidade:** `x1`.
- **Duração:** `8s`.

Essa baseline não substitui uma especificação aprovada para episódio ou cena.

## Registro pós-geração

Após gerar, criar ou atualizar o registro em `producao/testes/` com:

- ferramenta e configuração;
- prompt ID e versão;
- referências realmente fornecidas;
- resultado observado;
- erros factuais;
- hipóteses separadas dos fatos;
- solução testada;
- dimensão aprovada;
- impacto no cânone.
