# Template Mestre de Vídeo

**Status:** `FONTE OFICIAL`

Usar este arquivo para todo novo prompt de vídeo da Família Silva, principalmente no Google Flow/Veo. O prompt final deve ser autossuficiente: não pode depender de memória da ferramenta, de geração anterior ou de uma referência que não esteja anexada na execução atual.

Preencher somente com informação aprovada. Se um campo obrigatório não tiver fonte, registrar `A DEFINIR` e não inventar. Blocos sem aplicação real podem ser omitidos — **exceto o conteúdo de `FICTIONAL CONTEXT DECLARATION`, quando necessário, e o de `SERIES RENDERING STYLE CONTINUITY`, que é obrigatório em todo prompt de vídeo e nunca pode ser omitido, esvaziado ou enfraquecido, nem mesmo como tentativa de corrigir um bloqueio do Flow.** Ver "Bloqueios do Flow" abaixo.

## Regra central

**Documentation may be detailed. The final Google Flow prompt must be concise.**

Este documento tem duas camadas, e elas não se confundem:

1. **Estrutura interna de raciocínio e validação** — os blocos nomeados (`CHARACTER VISUAL CONTINUITY`, `SERIES RENDERING STYLE CONTINUITY`, `SPEAKING CONTINUITY`, etc.), a checklist e os erros conhecidos. Servem para a IA **pensar e validar** antes de escrever o prompt, e para registrar o teste em `producao/testes/`. **Nunca são copiados literalmente para o Flow.**
2. **Prompt final** — o texto que efetivamente é colado no Flow. Deve ser **prosa natural, enxuta, sem cabeçalhos técnicos, sem campos `A DEFINIR`, sem IDs, sem estrutura administrativa.** Ver "Do raciocínio interno ao prompt final" logo abaixo do template.

A IA usa a checklist para **validar** o prompt já escrito em prosa — nunca despeja a checklist ou os nomes dos blocos dentro do prompt entregue ao usuário.

## Metadados do registro

- **Prompt ID:** `PROMPT-CHAR-XXX-VIDEO-XXX`
- **Versão:** `VXX`
- **Status:** `EM TESTE`
- **Ferramenta/modelo:** `A DEFINIR`
- **Personagem(ns):** `A DEFINIR`
- **Cena/episódio:** `A DEFINIR`
- **Referências anexadas nesta geração:** `A DEFINIR`

## Estrutura interna de raciocínio e validação (NÃO é o prompt final)

**Esta estrutura, com cabeçalhos em maiúsculas, existe para organizar o raciocínio da IA e para preencher o registro em `producao/testes/`. Ela não deve ser copiada literalmente para o Flow.** Os cabeçalhos (`FICTIONAL CONTEXT DECLARATION`, `SCENE OBJECTIVE`, `CHARACTERS PRESENT`, `CURRENT GENERATION REFERENCES`, `TECHNICAL OUTPUT`, `FINAL CONTINUITY CHECK` etc.) são rótulos administrativos internos, não texto a ser enviado à ferramenta. Preencher todos os blocos aplicáveis aqui primeiro, depois seguir "Do raciocínio interno ao prompt final" para transformar isso em prosa.

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
Photorealistic / Warm Cinematic Realism. Mandatory in every prompt, never "live-action-adjacent" or any weaker equivalent: "Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment."
Use physically plausible materials, realistic depth of field, and grounded color.
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

## Do raciocínio interno ao prompt final

Depois de preencher a estrutura interna acima, reescreva-a como prosa natural em inglês antes de entregar ao usuário. Regras obrigatórias nessa transformação:

**A. Live-action explícito.** Todo prompt final deve conter, quase literalmente, a frase obrigatória: `"Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment."` Nunca substituir "live-action" por "live-action-adjacent" ou qualquer formulação mais fraca.

**B. Sem cabeçalhos administrativos.** Remover completamente rótulos como `FICTIONAL CONTEXT DECLARATION`, `SCENE OBJECTIVE`, `CHARACTERS PRESENT`, `CURRENT GENERATION REFERENCES`, `TECHNICAL OUTPUT`, `FINAL CONTINUITY CHECK` e qualquer outro cabeçalho em maiúsculas do prompt final. Eles são organização interna, não texto para o Flow. Converter cada regra aplicável em uma frase de prosa.

**C. Omitir campos não definidos.** Nunca escrever `Duration: A DEFINIR`, `Resolution: A DEFINIR`, `Frame rate: A DEFINIR`, `Generation quantity: A DEFINIR`, `Voice: A DEFINIR`, `Ambience: A DEFINIR` ou equivalente no prompt final. Se algo não foi definido e não é necessário para a geração pedida, **omitir a linha inteira**, não escrever o placeholder. Em especial, não incluir duração no prompt final quando o usuário não pediu uma duração específica — duração é configuração da ferramenta, não texto de prompt (ver "Baseline opcional" abaixo).

**D. Locks reduzidos a frases naturais.** Manter internamente os conceitos de `Speaking Lock`, `Voice Lock`, `Lip-Sync Lock` e `Silent Character Lock` como regras de validação, mas no prompt final reduzi-los a uma frase natural, por exemplo `"Only [NAME] speaks. No other voices are heard."` (personagem único) ou `"Only [NAME] speaks. Everyone else remains silent."` (múltiplos personagens). Não criar longas cadeias de proibições no prompt final, salvo se um erro específico e documentado justificar uma restrição adicional pontual.

**E. Fictional context com moderação.** Família Silva continua sendo obra ficcional original, mas não repetir automaticamente em todo prompt final longas frases sobre "real person", "likeness", "identity" ou "imitation". Usar esse contexto apenas quando realmente necessário para compliance (por exemplo, se uma geração anterior foi bloqueada por esse motivo). Esse contexto nunca pode enfraquecer o requisito de live-action photorealistic do item A.

**F. Referência MASTER concisa.** Usar o wording comprovado e enxuto: `"Use the uploaded master image(s) of [NAME(S)] as the visual reference and preserve their established appearance consistently."` Evitar blocos extensos sobre biometria, morphing ou identidade quando não houver necessidade específica documentada (ver `producao/solucoes/SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md`).

**G. Regra central, de novo.** Documentation may be detailed. The final Google Flow prompt must be concise. A checklist serve para validar o prompt já escrito, não para ser colada dentro dele.

O resultado deve ser um texto corrido, em inglês, com a fala em português brasileiro entre aspas, sem cabeçalhos, sem campos vazios e sem estrutura administrativa — pronto para colar diretamente no Flow. Ver os exemplos em "Reference Examples" abaixo.

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
- Os cabeçalhos em letras maiúsculas usados para estruturar a "Estrutura interna de raciocínio" (`SCENE OBJECTIVE`, `CHARACTERS PRESENT` etc.) são organização administrativa interna e **não devem ser copiados para o prompt final** (ver "Do raciocínio interno ao prompt final" acima) — não porque haja prova de que causem bloqueio (eles estavam presentes tanto no prompt que falhou quanto no que funcionou na Cena 2B, `ERR-007`, sem causalidade estabelecida), mas porque um prompt em prosa natural, enxuto, é o padrão exigido pela regra central deste template.

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

Esta checklist serve para **validar** o prompt final já escrito em prosa. Nunca copiar os itens da checklist, os nomes dos blocos ou os cabeçalhos internos para dentro do prompt entregue ao usuário.

- [ ] O prompt final está em prosa natural, sem os cabeçalhos em maiúsculas da estrutura interna (`FICTIONAL CONTEXT DECLARATION`, `SCENE OBJECTIVE`, `CHARACTERS PRESENT`, `TECHNICAL OUTPUT`, `FINAL CONTINUITY CHECK` etc.)?
- [ ] O prompt final não contém nenhuma linha `A DEFINIR` (campo não definido foi omitido, não escrito como placeholder)?
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
