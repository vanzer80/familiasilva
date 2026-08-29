# Template Mestre de Vídeo

**Status:** `FONTE OFICIAL`

Usar este arquivo para todo novo prompt de vídeo da Família Silva, principalmente no Google Flow/Veo e, quando aplicável, em outros geradores de vídeo compatíveis com as mesmas continuidades. O prompt final deve ser autossuficiente: não pode depender de memória da ferramenta, de geração anterior ou de uma referência que não esteja anexada na execução atual.

Preencher somente com informação aprovada. Se um campo obrigatório não tiver fonte, registrar `A DEFINIR` e não inventar. Blocos sem aplicação real podem ser omitidos — **exceto o conteúdo de `FICTIONAL CONTEXT DECLARATION`, quando necessário, e o de `SERIES RENDERING STYLE CONTINUITY`, que é obrigatório em todo prompt de vídeo e nunca pode ser omitido, esvaziado ou enfraquecido, nem mesmo como tentativa de corrigir um bloqueio do Flow.** Ver "Bloqueios do Flow" abaixo.

## Regra central

**Documentation may be detailed. The final generation prompt must be concise.**

Este documento tem duas camadas, e elas não se confundem:

1. **Estrutura interna de raciocínio e validação** — os blocos nomeados (`CHARACTER VISUAL CONTINUITY`, `SERIES RENDERING STYLE CONTINUITY`, `SPEAKING CONTINUITY`, etc.), a checklist e os erros conhecidos. Servem para a IA **pensar e validar** antes de escrever o prompt, e para registrar o teste em `producao/testes/`. **Nunca são copiados literalmente para a ferramenta de geração.**
2. **Prompt final** — o texto que efetivamente é colado no gerador. Deve ser **prosa natural, enxuta, sem cabeçalhos técnicos, sem campos `A DEFINIR`, sem IDs, sem estrutura administrativa.** Ver "Do raciocínio interno ao prompt final" logo abaixo do template.

A IA usa a checklist para **validar** o prompt já escrito em prosa — nunca despeja a checklist ou os nomes dos blocos dentro do prompt entregue ao usuário.

Antes de segmentar um roteiro em vários arquivos, aplicar também a regra de arquitetura multi-beat em [LRN-015](../../docs/APRENDIZADOS-DE-VIDEO.md#lrn-015--vídeo-contínuo-multi-beat-para-microcenas-encadeadas) / [DEC-018](../../docs/DECISOES.md#dec-018): microcenas causal ou emocionalmente conectadas devem ser avaliadas primeiro como beats de um único vídeo contínuo quando a plataforma e a complexidade da cena permitirem. Isso complementa, e não revoga, a arquitetura de microclipes.

## Metadados do registro

- **Prompt ID:** `PROMPT-CHAR-XXX-VIDEO-XXX`
- **Versão:** `VXX`
- **Status:** `EM TESTE`
- **Ferramenta/modelo:** `A DEFINIR`
- **Personagem(ns):** `A DEFINIR`
- **Cena/episódio:** `A DEFINIR`
- **Arquitetura:** `MICROCLIPE` ou `MULTI-BEAT`
- **Referências anexadas nesta geração:** `A DEFINIR`

## Estrutura interna de raciocínio e validação (NÃO é o prompt final)

**Esta estrutura, com cabeçalhos em maiúsculas, existe para organizar o raciocínio da IA e para preencher o registro em `producao/testes/`. Ela não deve ser copiada literalmente para o gerador.** Os cabeçalhos (`FICTIONAL CONTEXT DECLARATION`, `SCENE OBJECTIVE`, `CHARACTERS PRESENT`, `CURRENT GENERATION REFERENCES`, `TECHNICAL OUTPUT`, `FINAL CONTINUITY CHECK` etc.) são rótulos administrativos internos, não texto a ser enviado à ferramenta. Preencher todos os blocos aplicáveis aqui primeiro, depois seguir "Do raciocínio interno ao prompt final" para transformar isso em prosa.

```text
FICTIONAL CONTEXT DECLARATION
This video belongs to Família Silva, an original fictional Brazilian family sitcom. Every named character is an original fictional character. Use only the project-owned reference images attached to this generation. Do not interpret any character as a real person and do not imitate a real person's likeness.

SCENE OBJECTIVE
[State the exact purpose of this shot or continuous multi-beat sequence.]

NARRATIVE ARCHITECTURE
[Choose MICROCLIP or MULTI-BEAT.]
[If MULTI-BEAT, list the beats in chronological order and explain the causal/emotional connection between them.]
[Prefer MULTI-BEAT when consecutive micro-scenes share a compatible temporal block, environment/costume continuity, and manageable dialogue assignment.]
[Use MICROCLIP when scene complexity, platform limits, visual drift, or speaking/lip-sync risk makes the longer generation less reliable.]

CHARACTERS PRESENT
[List only the characters who must be visible, by name and approved role in the scene. Character IDs stay in the metadata above; never write CHAR-XXX inside this text.]
[For an individual shot, state that only the requested character is visible.]
[For MULTI-BEAT, specify which characters are present in each beat if the visible cast changes.]

CURRENT GENERATION REFERENCES
[List each attached reference and the character, costume, or environment it belongs to. Use each character's current canonical MASTER V02 PHOTOREALISTIC — see assets/personagens/mestres/MANIFESTO-MESTRES.md — not the historical V01, unless a specific approved source requires otherwise.]
Use the uploaded master images as visual references and preserve their identities consistently. Each character must use only their own approved reference — never another character's.
[A prior approved video may guide only the specifically approved method or rendering dimension; it never replaces the character's own facial reference.]

CHARACTER VISUAL CONTINUITY
For each visible character, preserve the approved facial features, apparent age, hair, body build, height, proportions, silhouette, and distinguishing visual features shown in that character's own attached approved reference (current canon: MASTER V02 PHOTOREALISTIC). Because this reference is already photorealistic, the prompt does not need to "convert" a stylized/3D reference into live-action — only preserve what the reference already shows.
Maintain stable facial structure, body build, weight, anatomy, skin texture, hair, and proportions from the first frame to the last.
No facial drift, body drift, weight change, age change, morphing, feature blending, or character mixing.
[Add only approved character-specific details.]

SERIES RENDERING STYLE CONTINUITY
Photorealistic / Warm Cinematic Realism. Mandatory in every prompt, never "live-action-adjacent" or any weaker equivalent: "Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment."
Use physically plausible materials, realistic depth of field, and grounded color.
Avoid flat cartoon rendering, childlike animation, toy-like appearance, waxy or plastic skin, exaggerated proportions, and visual imitation of any named studio, franchise, artwork, or artist.

COSTUME CONTINUITY
[Describe only the approved costume attached to or documented for each character.]
Keep every garment, color, fabric, accessory, footwear item, fit, and state of wear stable for the full shot.
[For MULTI-BEAT within the same temporal block, preserve costume across all beats unless an approved narrative change explicitly requires otherwise.]
No spontaneous wardrobe or accessory changes.

ENVIRONMENT CONTINUITY
[Describe the approved location, layout, permanent objects, lighting, time of day, and continuity requirements.]
Keep architecture, furniture, props, object placement, colors, and lighting direction stable.
[For MULTI-BEAT, describe the transition between beats explicitly. Prefer the same environment or a simple, narratively justified transition; do not invent a large location/time jump merely to fill duration.]

SHOT, CAMERA, AND COMPOSITION
Format: [for example, vertical 9:16].
Framing: [A DEFINIR].
Camera position and movement: [A DEFINIR].
Lens and depth of field: [A DEFINIR].
Composition: [A DEFINIR].
[For MULTI-BEAT, define whether the sequence remains continuous or uses a natural transition between beats. The transition must serve story continuity, not create arbitrary montage.]
Do not introduce unrequested characters, objects, text, logos, cuts, or camera moves.

ACTION AND PERFORMANCE
[Describe the action in chronological order.]
[Describe approved expression, posture, gestures, reaction, and comedic timing.]
[For MULTI-BEAT, describe the emotional state entering each beat and how the preceding beat causes or changes the next one.]
Keep movement natural, physically plausible, restrained, and consistent with the character's canonical personality.

RELATIONSHIP CONTINUITY
[For scenes with multiple characters, state only the approved relationship, distance, form of address, and interaction dynamic needed in this scene.]
Do not infer or create a new relationship.

DIALOGUE MAP
[For MICROCLIP:]
Speaker: [Character name]
Exact dialogue in Brazilian Portuguese: "[LITERAL DIALOGUE]"
Voice source/status: [approved voice reference or A DEFINIR]

[For MULTI-BEAT, map dialogue per beat:]
Beat 1 — Speaker: [Character name]
Exact dialogue in Brazilian Portuguese: "[LITERAL DIALOGUE]"
Beat 1 — Silent characters: [names]

Beat 2 — Speaker: [Character name]
Exact dialogue in Brazilian Portuguese: "[LITERAL DIALOGUE]"
Beat 2 — Silent characters: [names]

[Repeat only as needed. Do not add unnecessary beats.]

SPEAKING AND VOICE
For a microclip, only the assigned character speaks and everyone else remains silent. For a MULTI-BEAT sequence, exclusivity applies per beat: only the character assigned to the current beat speaks; everyone else visible in that beat remains silent. Each line belongs only to its assigned speaker — never exchange, blend, redistribute, complete, or add dialogue or voices.

LIP-SYNC
Only the speaking character in the current beat shows lip movement, matching their exact Portuguese dialogue. Silent characters keep a closed, natural mouth and never mouth words as if speaking; they may still react through expression, eye movement, posture, and gesture. When the speaker changes in a later beat, the lip-sync assignment changes only at that beat transition.

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
Duration: [A DEFINIR]. Configure this in the tool; do not write a fixed second count (e.g. "8 seconds" or "20 seconds") inside the scene text above unless a specific platform workflow explicitly requires the duration in prompt text.
Aspect ratio: [A DEFINIR].
Resolution: [A DEFINIR].
Frame rate: [A DEFINIR].
Number of shots/beats: [A DEFINIR].
Audio enabled: [A DEFINIR].
Generation quantity: [A DEFINIR].

FINAL CONTINUITY CHECK
Generate only the described original fictional scene. Preserve every supplied approved reference and every dialogue assignment. In MULTI-BEAT mode, preserve continuity and causal/emotional progression between beats and keep speaking/lip-sync ownership correct inside each beat. When an instruction is not defined above, do not invent a new canonical character trait, relationship, costume, voice, prop, or location.
```

## Do raciocínio interno ao prompt final

Depois de preencher a estrutura interna acima, reescreva-a como prosa natural em inglês antes de entregar ao usuário. Regras obrigatórias nessa transformação:

**A. Live-action explícito.** Todo prompt final deve conter, quase literalmente, a frase obrigatória: `"Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment."` Nunca substituir "live-action" por "live-action-adjacent" ou qualquer formulação mais fraca.

**B. Sem cabeçalhos administrativos.** Remover completamente rótulos como `FICTIONAL CONTEXT DECLARATION`, `SCENE OBJECTIVE`, `CHARACTERS PRESENT`, `TECHNICAL OUTPUT`, `FINAL CONTINUITY CHECK` e qualquer outro cabeçalho em maiúsculas do prompt final. Eles são organização interna, não texto para a ferramenta. Converter cada regra aplicável em uma frase de prosa.

**C. Omitir campos não definidos.** Nunca escrever `Duration: A DEFINIR`, `Resolution: A DEFINIR`, `Frame rate: A DEFINIR`, `Generation quantity: A DEFINIR`, `Voice: A DEFINIR`, `Ambience: A DEFINIR` ou equivalente no prompt final. Se algo não foi definido e não é necessário para a geração pedida, **omitir a linha inteira**, não escrever o placeholder. Em especial, não transformar a duração observada em um teste (`8s`, `20s` ou outra) em regra textual universal; duração é preferencialmente configuração da ferramenta.

**D. Locks reduzidos a frases naturais.** Manter internamente os conceitos de `Speaking Lock`, `Voice Lock`, `Lip-Sync Lock` e `Silent Character Lock` como regras de validação, mas no prompt final reduzi-los a frases naturais. Em MICROCLIPE, por exemplo: `"Only [NAME] speaks. Everyone else remains silent."` Em MULTI-BEAT, declarar por beat: `"Only [NAME] speaks during this first beat..."`, seguido da atribuição correspondente no próximo beat. Não criar longas cadeias de proibições no prompt final, salvo se um erro específico e documentado justificar uma restrição adicional pontual.

**E. Fictional context com moderação.** Família Silva continua sendo obra ficcional original, mas não repetir automaticamente em todo prompt final longas frases sobre "real person", "likeness", "identity" ou "imitation". Usar esse contexto apenas quando realmente necessário para compliance (por exemplo, se uma geração anterior foi bloqueada por esse motivo). Esse contexto nunca pode enfraquecer o requisito de live-action photorealistic do item A.

**F. Referência MASTER concisa.** Usar o wording comprovado e enxuto: `"Use the uploaded master image(s) of [NAME(S)] as the visual reference and preserve their established appearance consistently."` Anexar sempre a MASTER `V02 PHOTOREALISTIC` de cada personagem (current canon desde a [DEC-015](../../docs/DECISOES.md#dec-015) — ver [MANIFESTO-MESTRES.md](../../assets/personagens/mestres/MANIFESTO-MESTRES.md)), não a V01 histórica. Como a V02 já é fotorrealista, o prompt não precisa converter uma referência estilizada em live-action — só preservar o que a própria referência já mostra. Evitar blocos extensos sobre biometria, morphing ou identidade quando não houver necessidade específica documentada (ver `producao/solucoes/SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md`).

**G. Regra central, de novo.** Documentation may be detailed. The final generation prompt must be concise. A checklist serve para validar o prompt já escrito, não para ser colada dentro dele.

O resultado deve ser um texto corrido, em inglês, com a fala em português brasileiro entre aspas, sem cabeçalhos, sem campos vazios e sem estrutura administrativa — pronto para colar diretamente na ferramenta de geração.

## Arquitetura preferencial condicional — vídeo contínuo multi-beat

Desde `2026-08-29`, [DEC-018](../../docs/DECISOES.md#dec-018) e [LRN-015](../../docs/APRENDIZADOS-DE-VIDEO.md#lrn-015--vídeo-contínuo-multi-beat-para-microcenas-encadeadas) orientam um upgrade de pipeline: **não dividir automaticamente cada microcena em um vídeo separado**.

Antes de escrever o prompt, perguntar internamente:

1. O segundo momento existe por causa do primeiro ou representa consequência emocional/narrativa direta?
2. Os beats compartilham o mesmo núcleo de ambiente, faixa temporal e figurino, ou exigem apenas uma transição simples e clara?
3. O elenco e a atribuição de fala permanecem controláveis por beat?
4. A plataforma disponível suporta uma duração suficiente sem degradar identidade, ação, fala ou lip sync?

Se a resposta for positiva, preferir um único prompt em prosa que use uma formulação equivalente a:

```text
Create one continuous vertical 9:16 video with two connected dramatic-comedic beats, keeping smooth continuity of character appearance, costume, environment and emotional progression.

First beat: [action, emotional state, exact dialogue, who speaks, who remains silent].

Then, without abrupt interruption, continue naturally into the second beat: [consequence/action, exact dialogue, who speaks, who remains silent].

The emotional progression must be clear: [state how beat 1 causes or transforms beat 2].
```

Esse exemplo é de **arquitetura**, não texto fixo. Adaptar à cena e manter o prompt enxuto.

### Quando NÃO agrupar

Manter ou voltar a microclipes quando houver:

- mudança grande de ambiente, horário ou figurino;
- elenco ou ações simultâneas demais;
- diálogo sobreposto ou alto risco de troca de fala, voz ou lip sync;
- deriva visual/narrativa no vídeo mais longo;
- plataforma sem duração/configuração adequada;
- resultado empiricamente pior do que a versão curta.

O formato multi-beat é um padrão preferencial **condicional**, não uma obrigação mecânica. O conhecimento acumulado com microclipes continua válido como fallback.

## Baseline opcional para teste curto no Flow

Quando o objetivo for repetir a configuração já validada de teste curto no Flow, preencher:

- **Fluxo:** `Vídeo → Elementos`.
- **Referências:** anexadas como Elementos, não Frames.
- **Modelo:** `Veo 3.1 Lite`.
- **Proporção:** `9:16`.
- **Quantidade:** `x1`.
- **Duração:** `8s`.

Essa baseline não substitui uma especificação aprovada para episódio ou cena e não limita o uso de vídeos mais longos em outras ferramentas. O teste multi-beat no Gemini demonstrou aproximadamente `20s`, mas isso é capacidade observada daquela geração, não baseline universal.

## Bloqueios do Flow — como corrigir sem sacrificar o realismo

Se o Flow rejeitar ou bloquear uma geração, a causa mais provável, segundo os erros documentados abaixo, é duração fixa em segundos, Character IDs no corpo do texto, linguagem biométrica rígida na referência MASTER, ou uma lista longa de negative constraints — não a ausência de realismo. Ao corrigir:

- **Nunca remova, esvazie ou enfraqueça `SERIES RENDERING STYLE CONTINUITY`** para tentar destravar a geração. Isso é a causa documentada em `ERR-001`, não a solução.
- **Nunca reforce `FICTIONAL CONTEXT DECLARATION` com linguagem adicional de "cartoon", "animated", "stylized", "illustration" ou equivalente** como tentativa de correção. A declaração de ficção existe apenas para deixar claro que os personagens não são pessoas reais; ela nunca substitui nem compete com o bloco de rendering fotorrealista.
- Se especificamente a referência às imagens MASTER for o ponto bloqueado, o fallback seguro é simplificar `CURRENT GENERATION REFERENCES` para algo factual e não biométrico, por exemplo: `"Reference images are attached for each character; match their established appearance."` Não trocar por linguagem mais rígida (`EXACTLY the same person`, `absolute source of truth for identity`, `biometric identity`, `face cloning`) — esse foi exatamente o padrão que falhou em `ERR-007`.
- Reduzir `NEGATIVE CONSTRAINTS` para o mínimo necessário, conforme `LRN-012` em [docs/APRENDIZADOS-DE-VIDEO.md](../../docs/APRENDIZADOS-DE-VIDEO.md), continua sendo uma correção válida.
- Os cabeçalhos em letras maiúsculas usados para estruturar a "Estrutura interna de raciocínio" (`SCENE OBJECTIVE`, `CHARACTERS PRESENT` etc.) são organização administrativa interna e **não devem ser copiados para o prompt final** — não porque haja prova de que causem bloqueio, mas porque um prompt em prosa natural, enxuto, é o padrão exigido pela regra central deste template.

## Registro pós-geração

Após gerar, criar ou atualizar o registro em `producao/testes/` com:

- ferramenta e configuração;
- arquitetura `MICROCLIPE` ou `MULTI-BEAT`;
- prompt ID e versão;
- referências realmente fornecidas;
- duração/configuração efetivamente usada na ferramenta;
- resultado observado;
- erros factuais;
- hipóteses separadas dos fatos;
- solução testada;
- dimensão aprovada;
- impacto no cânone.

## Checklist antes de entregar qualquer prompt

Esta checklist serve para **validar** o prompt final já escrito em prosa. Nunca copiar os itens da checklist, os nomes dos blocos ou os cabeçalhos internos para dentro do prompt entregue ao usuário.

- [ ] Antes da segmentação, foi avaliado se microcenas conectadas podem ser agrupadas com segurança em um vídeo `MULTI-BEAT`?
- [ ] Se `MULTI-BEAT`, a relação causal/emocional entre os beats está explícita e a transição é natural?
- [ ] Se `MULTI-BEAT`, cada beat define claramente quem fala e quem permanece silencioso?
- [ ] Se o multi-beat aumentar risco de deriva, troca de fala ou complexidade, o prompt foi revertido para microclipes?
- [ ] O prompt final está em prosa natural, sem os cabeçalhos em maiúsculas da estrutura interna (`FICTIONAL CONTEXT DECLARATION`, `SCENE OBJECTIVE`, `CHARACTERS PRESENT`, `TECHNICAL OUTPUT`, `FINAL CONTINUITY CHECK` etc.)?
- [ ] O prompt final não contém nenhuma linha `A DEFINIR` (campo não definido foi omitido, não escrito como placeholder)?
- [ ] É explicitamente live-action?
- [ ] É explicitamente photorealistic?
- [ ] Fala em pessoas reais, textura de pele natural, câmera real?
- [ ] Segue `Photorealistic / Warm Cinematic Realism`?
- [ ] O bloco `SERIES RENDERING STYLE CONTINUITY` está presente por completo, sem ter sido removido, esvaziado ou enfraquecido (inclusive se a geração anterior falhou ou foi bloqueada)?
- [ ] Usa as imagens MASTER como referência visual, cada personagem só com a sua própria?
- [ ] Evita linguagem biométrica ou rígida de identidade (`EXACTLY the same person`, `absolute source of truth for identity`, `biometric identity`, `face cloning`)?
- [ ] Não transforma duração observada em teste em regra fixa dentro do texto da cena?
- [ ] Não contém Character IDs, nomes técnicos de clipe/cena ou outros rótulos administrativos dentro do corpo do prompt?
- [ ] Não contém cabeçalhos ou títulos que possam ser renderizados como texto na imagem?
- [ ] A fala está atribuída exclusivamente ao personagem correto no beat em que ocorre?
- [ ] Personagens secundários permanecem explicitamente silenciosos no beat correspondente, sem mover os lábios?
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

Estes exemplos mostram o **prompt final já em prosa** — o formato que deve ser entregue ao usuário, não a estrutura interna de raciocínio.

### Exemplo 1 — Personagem único, olhando para a câmera

```text
Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment. Use the uploaded master image of Marcos as the visual reference and preserve his established appearance consistently.

Marcos is alone, facing the camera directly in a medium shot at eye level. He speaks warmly and naturally to the viewer, with relaxed, restrained body language.

Only Marcos speaks. No other voices are heard. His lips match his exact dialogue in Brazilian Portuguese: "[Marcos's exact line, in Brazilian Portuguese]"

No subtitles, captions, logos, or on-screen text.
```

### Exemplo 2 — Dois personagens, um falando e um silencioso

Baseado no roteiro canônico da Cena 2B (`producao/solucoes/SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md`, item A — `SOURCE AVAILABLE`), aplicando o wording de referência MASTER validado no mesmo documento (item D).

```text
Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment. Use the uploaded master images of Carol and Beto as the visual reference and preserve their established appearances consistently.

Carol and Beto, a married couple, stand together in the kitchen. Carol looks at Beto with dry disbelief, pauses, then delivers her line in a deadpan, matter-of-fact tone. Beto reacts with a small, sheepish smile but stays silent.

Only Carol speaks. Everyone else remains silent. Her lips match her exact dialogue in Brazilian Portuguese: "O 'investidor' é seu primo, Beto. E a reunião é porque ele ainda não recebeu os cinquenta reais que você deve."

No subtitles, captions, logos, or on-screen text.
```

### Exemplo 3 — Dois beats contínuos, falante diferente por beat

Derivado do teste registrado em `producao/testes/TESTE-VIDEO-MULTIBEAT-GEMINI-S01E001-001.md`. O exemplo mostra a arquitetura; adaptar falas e detalhes à cena real.

```text
Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment. Use the uploaded master images of the visible characters as visual references and preserve their established appearance consistently.

Create one continuous vertical 9:16 video with two connected dramatic-comedic beats, keeping smooth continuity of character appearance, costume, environment and emotional progression.

First beat: [describe the first event and emotional state]. [NAME] says in Brazilian Portuguese: "[EXACT LINE]" Only [NAME] speaks during this first beat. Everyone else remains silent and reacts naturally.

Then, without abrupt interruption, continue naturally into the second beat as a direct consequence of the first. [Describe the second event and changed emotional state]. [SECOND NAME] says in Brazilian Portuguese: "[EXACT LINE]" Only [SECOND NAME] speaks during this second beat. Everyone else remains silent and reacts naturally.

The emotional progression must be clear: [explain how the first beat causes or transforms the second]. Keep performances grounded and believable. No subtitles, captions, logos or visible text.
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
   Correção: `DIALOGUE MAP` explícito por personagem + exclusividade de fala por microclipe ou por beat em arquitetura multi-beat.

4. **Prompt dependente de contexto anterior** (`producao/erros/ERR-004-PROMPT-DEPENDENTE-DE-CONTEXTO.md`)
   Causa: instrução como "igual ao vídeo aprovado" sem repetir os atributos nem fornecer a referência na geração atual — o gerador não tem memória confiável de prompt ou vídeo anterior.
   Correção: todo prompt deve ser autossuficiente; repetir cada fato e referência necessários na própria geração.

5. **Referência facial cruzada** (`producao/erros/ERR-005-REFERENCIA-FACIAL-CRUZADA.md`)
   Causa: risco de um personagem usar traço visual de outro quando referências se misturam.
   Correção: cada personagem usa exclusivamente sua própria imagem MASTER; Sr. Antônio e Beto são referência apenas metodológica (arquitetura de prompt/rendering), nunca facial de outros.

6. **Referência de personagem não neutra** (`producao/erros/ERR-006-REFERENCIA-DUDU-NAO-NEUTRA.md`)
   Causa: imagem de referência com elementos que vazam para o vídeo gerado (gimbal/celular em quadro, boca aberta, calçado de marca).
   Correção: usar referência neutra, sem esses elementos, antes de aprovar (`producao/solucoes/SOL-006-REFERENCIA-NEUTRA-DUDU.md`).

7. **Texto, ID ou rótulo técnico aparecendo no vídeo** (`producao/erros/ERR-007-CENA-2B-TENTATIVA-INICIAL.md`)
   Causa: Character IDs (`CHAR-00X`) e duração fixa (`approximately 8-second`) escritos dentro do corpo do prompt enviado ao Flow, além de blocos de restrição extensos e wording de identidade rígido (`absolute source of truth for identity`, `preserve the exact same face`).
   Correção (`producao/solucoes/SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md`): remover IDs e duração do texto da cena, usar wording conciso de referência MASTER e manter a lista de `Negative Constraints` curta.

8. **Vídeo multi-beat complexo demais**
   Risco: agrupar beats sem causalidade, com mudança grande de ambiente/tempo/figurino, elenco excessivo ou múltiplas falas concorrentes pode aumentar deriva visual e erro de speaking/lip-sync.
   Correção: aplicar [LRN-015](../../docs/APRENDIZADOS-DE-VIDEO.md#lrn-015--vídeo-contínuo-multi-beat-para-microcenas-encadeadas); agrupar apenas beats compatíveis e voltar a microclipes quando a complexidade superar o benefício de continuidade.
