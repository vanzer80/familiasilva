# TESTE — Vídeo multi-beat contínuo no Gemini — S01E001

- **Data:** `2026-08-29`
- **Episódio:** `S01E001 — A Greve da Patrícia`
- **Ferramenta:** Gemini, opção de geração de vídeo
- **Modelo exato:** `A DEFINIR`
- **Configuração exata além da duração observada:** `A DEFINIR`
- **Status:** `APROVADO COMO EVIDÊNCIA DE ARQUITETURA DE GERAÇÃO`; não aprova automaticamente voz, mídia final, modelo ou duração universal

## Objetivo

Testar se duas microcenas narrativamente contíguas podem ser geradas dentro de um único vídeo mais longo, preservando as continuidades já aprendidas no projeto e reduzindo a sensação de cortes fragmentados entre cenas que pertencem ao mesmo momento dramático.

## Teste 1 — Marcos + Patrícia → Dudu + Patrícia

O usuário informou que a opção de geração de vídeo do Gemini permitiu gerar um vídeo de `20 segundos` e reuniu, na mesma geração, dois beats consecutivos do episódio:

1. Marcos pergunta a Patrícia pela pasta azul.
2. Em seguida, Dudu pergunta a Patrícia pela camiseta preta.

Patrícia participa dos dois beats, e as duas ações pertencem ao mesmo momento doméstico da manhã.

### Resultado observado

Segundo avaliação direta do usuário, a transição entre as duas cenas ficou **muito mais fluida** quando gerada no mesmo vídeo.

O prompt exato usado pelo usuário neste primeiro teste não foi importado para o repositório e permanece `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA`. Não reconstruir esse texto por suposição.

## Teste 2 — Patrícia declara a greve → Marcos sente a consequência

Foi então construído um prompt único para dois beats diretamente causais:

1. Patrícia chega ao limite e declara a greve doméstica diante de Marcos e Dudu.
2. Mais tarde na mesma manhã, Marcos procura a chave reserva, pede uma exceção e percebe que Patrícia está realmente mantendo a greve.

O prompt foi estruturado como **um vídeo contínuo com dois beats dramático-cômicos conectados**, preservando MASTERs próprias, rendering canônico, ambiente doméstico, progressão emocional, atribuição de fala e silêncio por beat.

### Prompt usado no segundo teste

```text
Use the uploaded master images of Patrícia, Marcos and Dudu as visual references and preserve their established appearance consistently.

Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment.

Create one continuous vertical 9:16 video with two connected dramatic-comedic beats inside the same modest middle-class Brazilian family home, keeping smooth continuity of character appearance, costume, environment and emotional progression.

First beat: inside the family's modest living room shortly after the kitchen incidents in the morning. Patrícia has reached her limit after spending the whole morning being treated as the person who must find, remember, prepare and solve everything for everyone. She faces Marcos and Dudu. At first she tries to stay controlled, but the frustration she has been holding back finally comes out in a real, spontaneous and emotional way, not theatrical. Patrícia says in Brazilian Portuguese: "Chega! Chega, gente! Hoje eu não procuro, não lembro, não preparo e não resolvo mais nada pra ninguém. A partir de agora, eu tô de greve!" Only Patrícia speaks during this first beat. Marcos and Dudu remain silent, reacting with surprise. Marcos is caught off guard and unsure how seriously to take it. Dudu freezes, realizing this may affect him too.

Then, without abrupt interruption, continue naturally into the second beat later that same morning in the same house, showing that Patrícia's strike is now real and already affecting the routine. Marcos has been searching for the spare house key for a while. He checks a drawer, looks around the room, searches another familiar place and becomes progressively more frustrated because he is used to Patrícia immediately knowing where everything is. Patrícia is sitting calmly nearby and deliberately does not help him. She is no longer arguing; she is simply following through on her strike. After failing to find the key, Marcos turns to her, frustrated but also slightly pleading, and says in Brazilian Portuguese: "Tá, Patrícia... eu entendi que tu tá de greve. Mas a chave reserva sumiu mesmo! Tu não vai me dar nem uma pista?" Only Marcos speaks during this second beat. Patrícia remains completely silent and gives him a calm, firm look that makes it clear there will be no exception.

The emotional progression must be very clear: first Patrícia explodes after accumulated frustration, then Marcos experiences the first real consequence of depending on her for everyday problems. The comedy should come from the truth of the family dynamic, not exaggerated acting. Keep performances natural, grounded and believable. Use subtle domestic ambience only. No music, subtitles, captions, logos or visible text.
```

### Resultado observado

Após a geração, o usuário avaliou o resultado como **"bom demais"** e pediu que o padrão fosse documentado e passasse a orientar as próximas gerações.

A duração binária do segundo resultado, o arquivo final e seus metadados ainda não foram auditados neste repositório. Portanto, não afirmar que todo resultado multi-beat terá exatamente 20 segundos nem que toda plataforma oferece a mesma janela.

## Aprendizado validado

Quando duas ou mais microcenas:

- são diretamente causais ou emocionalmente encadeadas;
- compartilham o mesmo ambiente ou uma transição simples dentro do mesmo núcleo;
- preservam o mesmo bloco temporal e figurino;
- têm elenco controlável e falas claramente atribuídas por beat;

é preferível **avaliar primeiro a geração como um vídeo contínuo multi-beat**, em vez de dividir automaticamente cada microcena em um vídeo separado.

## Preservação do conhecimento anterior

Este teste **não revoga** nenhum aprendizado anterior:

- a arquitetura de microclipes continua válida como fallback;
- `LRN-011` continua válido: o risco de troca de fala deve ser reduzido; em multi-beat, a atribuição de fala passa a ser controlada **por beat**, não necessariamente por vídeo inteiro;
- MASTER V02 própria de cada personagem continua obrigatória;
- `Photorealistic / Warm Cinematic Realism` continua obrigatório;
- continuidade de personagem, figurino, ambiente, relacionamento, fala, voz, lip sync e silêncio continuam válidas;
- simplificação controlada do prompt continua válida;
- duração continua sendo configurada na ferramenta e não deve virar regra fixa escrita no corpo do prompt.

## Critério de fallback para microclipes

Dividir novamente em vídeos menores quando houver:

- mudança grande de ambiente, tempo ou figurino;
- excesso de personagens ou ações concorrentes;
- diálogo sobreposto ou risco alto de troca de fala/voz/lip sync;
- deriva visual ou narrativa no vídeo mais longo;
- incompatibilidade da plataforma com a duração necessária;
- resultado inferior ao obtido com microclipes.

## Dimensão aprovada

`ARQUITETURA DE GERAÇÃO / CONTINUIDADE NARRATIVA ENTRE BEATS`.

Este registro não canoniza voz, duração universal, modelo específico do Gemini ou um arquivo final de episódio.

## Referências

- [TEMPLATE-MESTRE-VIDEO.md](../../prompts/templates/TEMPLATE-MESTRE-VIDEO.md)
- [APRENDIZADOS-DE-VIDEO.md](../../docs/APRENDIZADOS-DE-VIDEO.md)
- [DEC-018](../../docs/DECISOES.md#dec-018)
