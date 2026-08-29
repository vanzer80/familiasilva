# TESTE — Arquitetura multi-beat / Gemini — S01E001

- **Data:** `2026-08-29`
- **Episódio:** `S01E001 — A Greve da Patrícia`
- **Ferramenta:** Gemini, opção de geração de vídeo
- **Modelo exato:** `A DEFINIR`
- **Status atual:** `VALIDADO COMO EVIDÊNCIA NARRATIVA; MECANISMO DE 20s NÃO DETERMINADO`

## Objetivo original

Testar se microcenas narrativamente contíguas poderiam ser tratadas como uma sequência mais fluida, preservando as continuidades já aprendidas no projeto e reduzindo a sensação de cortes fragmentados.

## Teste 1 — Marcos + Patrícia → Dudu + Patrícia

O usuário produziu um resultado que reuniu dois beats consecutivos:

1. Marcos pergunta a Patrícia pela pasta azul.
2. Em seguida, Dudu pergunta a Patrícia pela camiseta preta.

Segundo avaliação direta do usuário, a transição entre os momentos ficou muito mais fluida.

### Auditoria posterior

O arquivo final correspondente, recebido e auditado nesta sessão como `1(1).mp4`, possui:

- duração: `20.010 s`;
- resolução: `720x1280`;
- frame rate: `24 fps`;
- vídeo: H.264;
- áudio: AAC estéreo `48 kHz`;
- SHA-256: `94eda5b740c994d78885b2e0b52f3c8be38c3997c0c672053865038b6e922f3d`.

### Correção de interpretação

A primeira versão deste registro afirmou que o Gemini havia produzido diretamente `20 segundos` em uma única geração. Essa formulação foi feita cedo demais.

Posteriormente, o próprio usuário levantou a possibilidade de ter produzido uma sequência/continuação. A existência do arquivo de `20.010 s` é fato; **o binário não permite determinar sozinho se sua origem foi geração única, extensão, continuação ou sequência na interface**.

Portanto:

- `20.010 s` do arquivo final = `CONFIRMADO`;
- benefício narrativo da sequência = `APROVADO`;
- “Gemini gera 20s diretamente em uma única geração nesse fluxo” = `NÃO COMPROVADO`.

O prompt exato usado pelo usuário neste primeiro resultado não foi importado para o repositório e permanece `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA`.

## Teste 2 — Patrícia declara a greve → Marcos sente a consequência

Foi construído um prompt único com dois beats diretamente causais:

1. Patrícia declara a greve diante de Marcos e Dudu.
2. Marcos procura a chave reserva e percebe que a greve terá consequência real.

O prompt de teste foi:

```text
Use the uploaded master images of Patrícia, Marcos and Dudu as visual references and preserve their established appearance consistently.

Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment.

Create one continuous vertical 9:16 video with two connected dramatic-comedic beats inside the same modest middle-class Brazilian family home, keeping smooth continuity of character appearance, costume, environment and emotional progression.

First beat: inside the family's modest living room shortly after the kitchen incidents in the morning. Patrícia has reached her limit after spending the whole morning being treated as the person who must find, remember, prepare and solve everything for everyone. She faces Marcos and Dudu. At first she tries to stay controlled, but the frustration she has been holding back finally comes out in a real, spontaneous and emotional way, not theatrical. Patrícia says in Brazilian Portuguese: "Chega! Chega, gente! Hoje eu não procuro, não lembro, não preparo e não resolvo mais nada pra ninguém. A partir de agora, eu tô de greve!" Only Patrícia speaks during this first beat. Marcos and Dudu remain silent, reacting with surprise. Marcos is caught off guard and unsure how seriously to take it. Dudu freezes, realizing this may affect him too.

Then, without abrupt interruption, continue naturally into the second beat later that same morning in the same house, showing that Patrícia's strike is now real and already affecting the routine. Marcos has been searching for the spare house key for a while. He checks a drawer, looks around the room, searches another familiar place and becomes progressively more frustrated because he is used to Patrícia immediately knowing where everything is. Patrícia is sitting calmly nearby and deliberately does not help him. She is no longer arguing; she is simply following through on her strike. After failing to find the key, Marcos turns to her, frustrated but also slightly pleading, and says in Brazilian Portuguese: "Tá, Patrícia... eu entendi que tu tá de greve. Mas a chave reserva sumiu mesmo! Tu não vai me dar nem uma pista?" Only Marcos speaks during this second beat. Patrícia remains completely silent and gives him a calm, firm look that makes it clear there will be no exception.

The emotional progression must be very clear: first Patrícia explodes after accumulated frustration, then Marcos experiences the first real consequence of depending on her for everyday problems. The comedy should come from the truth of the family dynamic, not exaggerated acting. Keep performances natural, grounded and believable. Use subtle domestic ambience only. No music, subtitles, captions, logos or visible text.
```

O resultado foi inicialmente avaliado pelo usuário como muito bom. Em teste posterior com outra combinação de duas cenas dentro de um arquivo de aproximadamente `10.005 s`, parte do diálogo foi cortada, demonstrando que **a arquitetura multi-beat só funciona quando a duração real comporta fala, ação, emoção e reação**.

## Aprendizado corrigido

Quando duas ou mais microcenas são diretamente causais ou emocionalmente encadeadas, vale avaliar uma sequência contínua porque isso pode melhorar fluidez. Porém:

- não presumir duração disponível;
- não presumir que um arquivo longo veio de uma única geração direta;
- medir a quantidade de fala pela janela real;
- voltar a microclipes ou usar uma continuação realmente suportada quando necessário.

## Aprendizado adicional de referências

Durante a mesma rodada, uma geração falhou porque nem todas as MASTERs pedidas estavam anexadas. Depois de anexar o conjunto completo, a geração funcionou. O usuário também validou que, no Gemini multi-reference, a ordem dos anexos deve acompanhar a ordem dos nomes no prompt para reduzir inversões de papel/fala.

Ver [ERR-009](../erros/ERR-009-GEMINI-MASTERS-AUSENTES-OU-FORA-DE-ORDEM.md) e [SOL-009](../solucoes/SOL-009-GEMINI-MASTERS-COMPLETAS-E-ORDENADAS.md).

## Preservação do conhecimento anterior

Continuam válidos:

- microclipes como fallback;
- `LRN-011` para controle de falantes;
- MASTER V02 própria de cada personagem;
- `Photorealistic / Warm Cinematic Realism`;
- continuidade de personagem, figurino, ambiente, relacionamento, fala, voz, lip sync e silêncio;
- simplificação controlada;
- duração tratada como configuração real da ferramenta, não como pressuposto textual.

## Dimensão aprovada

`ARQUITETURA NARRATIVA / CONTINUIDADE ENTRE BEATS`, condicionada à duração e à ferramenta.

Não está aprovado neste registro um mecanismo universal de geração direta de `20s` no Gemini.

## Referências

- [TEMPLATE-MESTRE-VIDEO.md](../../prompts/templates/TEMPLATE-MESTRE-VIDEO.md)
- [APRENDIZADOS-DE-VIDEO.md](../../docs/APRENDIZADOS-DE-VIDEO.md)
- [APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md](../../docs/APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md)
- [DEC-018 / DEC-019](../../docs/DECISOES.md)
