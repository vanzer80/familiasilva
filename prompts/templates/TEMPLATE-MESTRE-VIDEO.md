# Template Mestre de Vídeo

**Status:** `FONTE OFICIAL`

Usar este arquivo para todo novo prompt de vídeo da Família Silva, principalmente no Google Flow/Veo. O prompt final deve ser autossuficiente: não pode depender de memória da ferramenta, de geração anterior ou de uma referência que não esteja anexada na execução atual.

Preencher somente com informação aprovada. Se um campo obrigatório não tiver fonte, registrar `A DEFINIR` e não inventar. Blocos sem aplicação real podem ser omitidos — **exceto `FICTIONAL CONTEXT DECLARATION` e `SERIES RENDERING STYLE CONTINUITY`, que são obrigatórios em todo prompt de vídeo e nunca podem ser omitidos, esvaziados ou enfraquecidos, nem mesmo como tentativa de corrigir um bloqueio do Flow.** Ver "Bloqueios do Flow" abaixo.

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
[List only the characters who must be visible, by name and approved role in the scene. Character IDs stay in the metadata above; never write CHAR-XXX inside this text.]
[For an individual shot, state that only the requested character is visible.]

CURRENT GENERATION REFERENCES
[List each attached reference and the character, costume, or environment it belongs to.]
Use the uploaded master images as visual references and preserve their identities consistently. Each character must use only their own approved reference — never another character's.
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
Speaker: [Character name]
Exact dialogue in Brazilian Portuguese: "[LITERAL DIALOGUE]"
Voice source/status: [approved voice reference or A DEFINIR]

[Repeat the two lines above for every speaker.]

SPEAKING AND VOICE
Only [CHARACTER] speaks. Everyone else remains silent. Each line belongs only to its assigned speaker, using that character's own approved voice — never exchange, blend, redistribute, complete, or add dialogue or voices.

LIP-SYNC
Only the speaking character shows lip movement, matching their exact Portuguese dialogue. Silent characters keep a closed, natural mouth and never mouth words as if speaking; they may still react through expression, eye movement, posture, and gesture.

AUDIO
Dialogue: clear Brazilian Portuguese, foreground and intelligible.
Ambience: [A DEFINIR].
Music: [A DEFINIR or none].
Sound effects: [A DEFINIR or none].
No extra voices, narration, crowd speech, or unrequested vocal sounds.

NEGATIVE CONSTRAINTS
No extra limbs, fingers, or duplicated people; no deformed hands; no unrequested characters, cuts, or camera moves.
[Add only case-specific restrictions supported by an approved source. Most defects already have a positive rule above — Character Visual Continuity, Costume Continuity, Environment Continuity, Series Rendering Style Continuity, and Speaking/Voice/Lip-Sync — so do not restate them here. A short, targeted list works better than a long one.]

OUTPUT CLEANLINESS
No subtitles, captions, on-screen text, logos, watermarks, visible character IDs, or administrative clip/scene labels (for example "CHAR-005" or "Clip 2B").

TECHNICAL OUTPUT
Duration: [A DEFINIR]. Configure this in the tool; do not write a fixed second count (e.g. "8 seconds") inside the scene text above.
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

## Bloqueios do Flow — como corrigir sem sacrificar o realismo

Se o Flow rejeitar ou bloquear uma geração, a causa mais provável, segundo os erros documentados abaixo, é duração fixa em segundos, Character IDs no corpo do texto, linguagem biométrica rígida na referência MASTER, ou uma lista longa de negative constraints — não a ausência de realismo. Ao corrigir:

- **Nunca remova, esvazie ou enfraqueça `SERIES RENDERING STYLE CONTINUITY`** para tentar destravar a geração. Isso é a causa documentada em `ERR-001`, não a solução.
- **Nunca reforce `FICTIONAL CONTEXT DECLARATION` com linguagem adicional de "cartoon", "animated", "stylized", "illustration" ou equivalente** como tentativa de correção. A declaração de ficção existe apenas para deixar claro que os personagens não são pessoas reais; ela nunca substitui nem compete com o bloco de rendering fotorrealista.
- Se especificamente a referência às imagens MASTER for o ponto bloqueado, o fallback seguro é simplificar `CURRENT GENERATION REFERENCES` para algo factual e não biométrico, por exemplo: `"Reference images are attached for each character; match their established appearance."` Não trocar por linguagem mais rígida (`EXACTLY the same person`, `absolute source of truth for identity`, `biometric identity`, `face cloning`) — esse foi exatamente o padrão que falhou em `ERR-007`.
- Reduzir `NEGATIVE CONSTRAINTS` para o mínimo necessário, conforme `LRN-012` em [docs/APRENDIZADOS-DE-VIDEO.md](../../docs/APRENDIZADOS-DE-VIDEO.md), continua sendo uma correção válida.
- Nota sobre os cabeçalhos em letras maiúsculas usados para estruturar este template (`SCENE OBJECTIVE`, `CHARACTERS PRESENT` etc.): eles já estavam presentes tanto no prompt que falhou quanto no que funcionou no caso da Cena 2B (`ERR-007`), então não há evidência de que sejam a causa de bloqueio ou de texto em tela. Ainda assim, isso não foi comprovado como seguro de forma definitiva — permanece `A DEFINIR` como hipótese em aberto, não como regra validada.

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

## Checklist antes de entregar qualquer prompt

- [ ] É explicitamente live-action?
- [ ] É explicitamente photorealistic?
- [ ] Fala em pessoas reais, textura de pele natural, câmera real?
- [ ] Segue `Photorealistic / Warm Cinematic Realism`?
- [ ] O bloco `SERIES RENDERING STYLE CONTINUITY` está presente por completo, sem ter sido removido, esvaziado ou enfraquecido (inclusive se a geração anterior falhou ou foi bloqueada)?
- [ ] Usa as imagens MASTER como referência visual, cada personagem só com a sua própria?
- [ ] Evita linguagem biométrica ou rígida de identidade (`EXACTLY the same person`, `absolute source of truth for identity`, `biometric identity`, `face cloning`)?
- [ ] Não especifica duração fixa em segundos no texto da cena?
- [ ] Não contém Character IDs, nomes técnicos de clipe/cena ou outros rótulos administrativos dentro do corpo do prompt?
- [ ] Não contém cabeçalhos ou títulos que possam ser renderizados como texto na imagem?
- [ ] Apenas o personagem correto fala (`Only [CHARACTER] speaks. Everyone else remains silent.`)?
- [ ] Personagens secundários permanecem explicitamente silenciosos, sem mover os lábios?
- [ ] As falas estão em português brasileiro?
- [ ] As instruções estão em inglês?
- [ ] Não há texto, legenda, logo ou marca d'água na tela?
- [ ] Respeita `Character Visual Continuity`?
- [ ] Respeita `Costume Continuity`?
- [ ] Respeita `Environment Continuity`?
- [ ] A lista de `Negative Constraints` é curta e não repete o que já está garantido pelos blocos positivos acima?
- [ ] Foi comparado com os Reference Examples abaixo e com `docs/APRENDIZADOS-DE-VIDEO.md` antes de ser entregue?

## Reference Examples — illustrative, not production-verified

**Estes exemplos NÃO são prompts históricos aprovados.** Nenhum prompt historicamente aprovado tem seu texto literal recuperado neste repositório — nem de Sr. Antônio, nem de Beto, nem de nenhum outro personagem (todos os registros em `producao/testes/` e `producao/aprovados/` marcam o prompt exato como `A DEFINIR` ou `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA`; ver `producao/solucoes/SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md`, item D).

- Os exemplos abaixo são **derivados das regras consolidadas neste template**, não transcrições de produção.
- Eles **não são transcrições literais de nenhum prompt aprovado**.
- **Nenhum prompt histórico deve ser inventado ou apresentado como evidência de produção** — quando o texto exato de um prompt aprovado for importado para o repositório, ele substitui o exemplo correspondente aqui, com a fonte citada.

### Exemplo 1 — Personagem único, olhando para a câmera

```text
FICTIONAL CONTEXT DECLARATION
This video belongs to Família Silva, an original fictional Brazilian family sitcom. Every named character is an original fictional character. Use only the project-owned reference images attached to this generation. Do not interpret any character as a real person and do not imitate a real person's likeness.

SCENE OBJECTIVE
Marcos introduces himself directly to camera in his living room.

CHARACTERS PRESENT
Only Marcos is visible.

CURRENT GENERATION REFERENCES
Use the uploaded master images as visual references and preserve their identities consistently. Marcos uses only his own approved reference.

CHARACTER VISUAL CONTINUITY
Preserve Marcos's approved facial features, apparent age, hair, body build, and proportions from his own attached reference. No facial drift, body drift, weight change, or age change.

SERIES RENDERING STYLE CONTINUITY
Photorealistic / Warm Cinematic Realism. Natural skin texture, physically plausible materials, believable human anatomy, warm cinematic lighting, realistic depth of field, subtle live-action-adjacent polish. Avoid flat cartoon rendering, childlike animation, or plastic skin.

SHOT, CAMERA, AND COMPOSITION
Vertical 9:16. Medium shot, eye level, Marcos looking directly at the camera.

ACTION AND PERFORMANCE
Marcos smiles naturally and speaks directly to the camera with warm, relaxed body language.

DIALOGUE MAP
Speaker: Marcos
Exact dialogue in Brazilian Portuguese: "[LITERAL DIALOGUE — A DEFINIR]"

SPEAKING AND VOICE
Only Marcos speaks. Everyone else remains silent.

LIP-SYNC
Only Marcos shows lip movement, matching his exact Portuguese dialogue.

AUDIO
Dialogue: clear Brazilian Portuguese, foreground and intelligible.

OUTPUT CLEANLINESS
No subtitles, captions, on-screen text, logos, watermarks, visible character IDs, or administrative clip/scene labels (for example "CHAR-005" or "Clip 2B").

FINAL CONTINUITY CHECK
Generate only the described original fictional scene. Preserve every supplied approved reference and every dialogue assignment.
```

### Exemplo 2 — Dois personagens, um falando e um silencioso

Baseado no roteiro canônico da Cena 2B (`producao/solucoes/SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md`, item A — `SOURCE AVAILABLE`), aplicando o wording de referência MASTER validado no mesmo documento (item D).

```text
FICTIONAL CONTEXT DECLARATION
This video belongs to Família Silva, an original fictional Brazilian family sitcom. Every named character is an original fictional character. Use only the project-owned reference images attached to this generation. Do not interpret any character as a real person and do not imitate a real person's likeness.

SCENE OBJECTIVE
Carol explains to someone off-scene who the "investor" from Beto's meeting actually is.

CHARACTERS PRESENT
Carol and Beto are visible. Only Carol speaks; Beto remains silent.

CURRENT GENERATION REFERENCES
Use the uploaded master images as visual references and preserve their identities consistently. Each character uses only their own approved reference — never the other's.

CHARACTER VISUAL CONTINUITY
Preserve each character's approved facial features, apparent age, hair, body build, and proportions from their own attached reference. No facial drift, body drift, or character mixing between Carol and Beto.

SERIES RENDERING STYLE CONTINUITY
Photorealistic / Warm Cinematic Realism. Natural skin texture, believable human anatomy, warm cinematic lighting, realistic depth of field. Avoid flat cartoon rendering or plastic skin.

RELATIONSHIP CONTINUITY
Carol and Beto are married. Casual, familiar domestic interaction.

DIALOGUE MAP
Speaker: Carol
Exact dialogue in Brazilian Portuguese: "O 'investidor' é seu primo, Beto. E a reunião é porque ele ainda não recebeu os cinquenta reais que você deve."

SPEAKING AND VOICE
Only Carol speaks. Everyone else remains silent.

LIP-SYNC
Only Carol shows lip movement, matching her exact Portuguese dialogue. Beto keeps a closed, natural mouth and never mouths words; he may react through expression and posture.

AUDIO
Dialogue: clear Brazilian Portuguese, foreground and intelligible.

OUTPUT CLEANLINESS
No subtitles, captions, on-screen text, logos, watermarks, visible character IDs, or administrative clip/scene labels (for example "CHAR-005" or "Clip 2B").

FINAL CONTINUITY CHECK
Generate only the described original fictional scene. Preserve every supplied approved reference and every dialogue assignment.
```

## Erros conhecidos e como evitar regressões

1. **Cartoon / desenho / plástico** (`producao/erros/ERR-001-RENDERING-CARTOON.md`)
   Causa: rendering realista insuficientemente explícito; hipótese não comprovada de que nomear franquia/estúdio como atalho de estilo contribuiu.
   Correção: usar `Photorealistic / Warm Cinematic Realism` (bloco `SERIES RENDERING STYLE CONTINUITY`), descrever pele, materiais, anatomia, luz e câmera tecnicamente, nunca citando estúdio, franquia, obra ou artista.

2. **Deriva visual corporal** (`producao/erros/ERR-002-DERIVA-VISUAL-CORPORAL.md`)
   Causa: variação perceptível de compleição/peso entre gerações (caso Marcos).
   Correção: bloco `CHARACTER VISUAL CONTINUITY` explícito, proibindo morphing, mudança de peso e deriva facial do primeiro ao último frame.

3. **Fala, voz ou lip sync trocados** (`producao/erros/ERR-003-FALA-VOZ-LIPSYNC.md`)
   Causa: modelo atribui fala a personagem errado, troca voz, ou personagem completa a fala de outro.
   Correção: `DIALOGUE MAP` explícito por personagem + `Only [CHARACTER] speaks. Everyone else remains silent.` no bloco `SPEAKING AND VOICE`.

4. **Prompt dependente de contexto anterior** (`producao/erros/ERR-004-PROMPT-DEPENDENTE-DE-CONTEXTO.md`)
   Causa: instrução como "igual ao vídeo aprovado" sem repetir os atributos nem fornecer a referência na geração atual — o Flow não tem memória confiável de prompt ou vídeo anterior.
   Correção: todo prompt deve ser autossuficiente; repetir cada fato e referência necessários na própria geração.

5. **Referência facial cruzada** (`producao/erros/ERR-005-REFERENCIA-FACIAL-CRUZADA.md`)
   Causa: risco de um personagem usar traço visual de outro quando referências se misturam.
   Correção: cada personagem usa exclusivamente sua própria imagem MASTER; Sr. Antônio e Beto são referência apenas metodológica (arquitetura de prompt/rendering), nunca facial de outros.

6. **Referência de personagem não neutra** (`producao/erros/ERR-006-REFERENCIA-DUDU-NAO-NEUTRA.md`)
   Causa: imagem de referência com elementos que vazam para o vídeo gerado (gimbal/celular em quadro, boca aberta, calçado de marca).
   Correção: usar referência neutra, sem esses elementos, antes de aprovar (`producao/solucoes/SOL-006-REFERENCIA-NEUTRA-DUDU.md`).

7. **Texto, ID ou rótulo técnico aparecendo no vídeo** (`producao/erros/ERR-007-CENA-2B-TENTATIVA-INICIAL.md`)
   Causa: Character IDs (`CHAR-00X`) e duração fixa (`approximately 8-second`) escritos dentro do corpo do prompt enviado ao Flow, além de blocos de restrição extensos e wording de identidade rígido (`absolute source of truth for identity`, `preserve the exact same face`).
   Correção (`producao/solucoes/SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md`): remover IDs e duração do texto da cena, usar `use the uploaded master images as visual references and preserve their identities consistently`, e manter a lista de `Negative Constraints` curta.
