# Aprendizados de Vídeo

Este documento consolida o que foi aprendido nos testes audiovisuais da Família Silva. Ele não substitui as decisões formais nem o template mestre:

- [DECISOES.md](DECISOES.md) define o que é permanente e aprovado.
- [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md) define como construir cada novo prompt.
- [producao/](../producao/) preserva a evidência de testes, erros, soluções, aprovações e rejeições.

Hipóteses são identificadas como hipóteses. Campos sem evidência permanecem `A DEFINIR`.

## Regras consolidadas

### LRN-001 — Rendering realista em vez de cartoon

- **Observação:** resultados com cartoon, pele plástica ou aparência infantil se afastaram da direção desejada para a série.
- **Decisão resultante:** usar `Photorealistic / Warm Cinematic Realism` em todos os novos materiais visuais e audiovisuais.
- **Aplicação:** textura natural de pele, materiais plausíveis, anatomia crível, proporções humanas coerentes, iluminação quente cinematográfica e profundidade de campo realista.
- **Evitar:** cartoon plano, visual de brinquedo, pele encerada ou plástica, proporções exageradas e aparência infantil.
- **Status:** `VALIDADO` pela [DEC-003](DECISOES.md#dec-003).

### LRN-002 — Descrever o estilo tecnicamente

- **Observação:** usar nomes de estúdios, franquias, obras ou artistas como atalho pode produzir estilo indesejado e respostas inconsistentes.
- **Causa do caso Patrícia:** a associação com termo de franquia foi considerada uma causa provável, não comprovada, para o desvio de cartoon.
- **Solução:** descrever rendering, pele, materiais, iluminação, lente, profundidade de campo e anatomia sem citar marcas ou criadores.
- **Status:** `SOLUÇÃO ADOTADA`; causalidade específica permanece `HIPÓTESE`.

### LRN-003 — Todo prompt precisa ser autossuficiente

- **Observação:** o Flow não conhece prompts, imagens ou vídeos anteriores que não sejam fornecidos na geração atual.
- **Solução:** repetir no prompt todos os fatos necessários; não escrever “igual ao vídeo aprovado” ou instrução equivalente sem também fornecer os atributos e as referências atuais.
- **Status:** `VALIDADO` pela [DEC-004](DECISOES.md#dec-004).

### LRN-004 — Imagem MASTER própria por personagem

- **Observação:** referências cruzadas podem misturar rosto, corpo ou proporções entre personagens.
- **Solução:** cada personagem usa sua própria imagem MASTER ou referência explicitamente aprovada. Vídeos anteriores servem apenas como referência complementar da dimensão aprovada.
- **Regra especial:** Sr. Antônio e Beto são referências metodológicas de arquitetura de prompt e rendering; nunca referências faciais de outros personagens.
- **Status:** `VALIDADO` pela [DEC-005](DECISOES.md#dec-005).

### LRN-005 — Continuidade precisa ser explícita

- **Observação:** rosto, peso, corpo, cabelo, figurino e cenário podem variar entre gerações. No caso de Marcos, houve variação perceptível de compleição entre vídeos.
- **Solução:** declarar `Character Visual Continuity`, `Costume Continuity` e `Environment Continuity`, repetir os atributos aprovados e proibir morphing, mudança de peso, deriva facial e alteração de roupa durante o take.
- **Status:** `VALIDADO` como regra de produção; detalhes visuais não documentados continuam `A DEFINIR`.

### LRN-006 — Fala, voz e lip sync são vínculos diferentes

- **Observação:** modelos podem trocar falas, vozes ou movimentar os lábios de personagens silenciosos.
- **Solução:** atribuir cada fala literal a um personagem e declarar separadamente `Speaking Continuity`, `Voice Continuity`, `Lip-Sync Continuity` e `Silent Character Continuity`.
- **Status:** `VALIDADO` como regra obrigatória.

### LRN-007 — Aprovações não devem ser ampliadas

- **Observação:** um vídeo pode acertar o visual e ainda usar fala ou voz experimental.
- **Solução:** registrar separadamente aprovação visual, vocal, narrativa e técnica.
- **Exemplo:** o primeiro teste de Carol foi aprovado visualmente, sem canonizar sua fala experimental, voz ou dinâmica narrativa.
- **Status:** `VALIDADO` pela [DEC-006](DECISOES.md#dec-006).

### LRN-008 — Limitar personagens e ações ao solicitado

- **Observação:** elementos não pedidos aumentam o risco de personagens extras, trocas de atenção, fala incorreta e deriva visual.
- **Solução:** listar exatamente quem aparece, quem fala, quem permanece silencioso e o que cada pessoa faz. Quando a cena for individual, declarar que somente o personagem solicitado está visível.
- **Status:** `VALIDADO` como regra de composição.

### LRN-009 — Baseline técnico do teste no Flow

- **Configuração validada para testes curtos:** `Vídeo → Elementos`, referências adicionadas como Elementos, proporção `9:16`, `Veo 3.1 Lite`, quantidade `x1` e duração `8s`.
- **Limite:** esta é uma baseline de teste, não uma duração obrigatória para todos os episódios ou cenas.
- **Status:** `VALIDADO PARA TESTE`.

## Estado dos casos conhecidos

| Personagem | Estado visual registrado | Aprendizado preservado | Limites |
| --- | --- | --- | --- |
| Marcos (`CHAR-001`) | `APROVADO COM RESSALVAS` | preservar compleição, rosto, roupa e cenário; impedir variação de peso e morphing | voz e campos visuais não descritos continuam `A DEFINIR` |
| Dona Célia (`CHAR-002`) | `APROVADO COM RESSALVAS` | manter leitura de idade madura e preservar rugas, cabelo grisalho, óculos e roupa quando presentes na referência aprovada | voz não canônica; descrição detalhada depende da referência |
| Patrícia (`CHAR-003`) | `APROVADO COM RESSALVAS` | retirar atalhos de franquia e aplicar rendering realista técnico | causa exata do erro de cartoon não foi comprovada |
| Sr. Antônio (`CHAR-004`) | `APROVADO COM RESSALVAS` | caso metodológico para arquitetura de prompt e rendering | não é referência facial para outros; é vizinho, não integrante da família |
| Beto (`CHAR-005`) | `APROVADO COM RESSALVAS` | prompt autossuficiente, personagem único quando solicitado e referência própria | não é referência facial para outros |
| Carol (`CHAR-006`) | `APROVADO VISUALMENTE` | continuidade visual e rendering canônico validados | fala experimental, voz e dinâmica narrativa não canônicas |
| Dudu (`CHAR-007`) | `AJUSTE NECESSÁRIO` | referência neutra antes da aprovação | retirar gimbal/celular, manter boca fechada e tênis sem marca na nova referência |

Os registros detalhados ficam em [producao/testes/](../producao/testes/).

## Procedimento para novos aprendizados

1. Criar o registro em `producao/testes/` antes da geração ou da avaliação.
2. Registrar cada defeito em `producao/erros/`, distinguindo fato de hipótese.
3. Registrar a correção em `producao/solucoes/` e vinculá-la ao erro.
4. Só mover a conclusão para `producao/aprovados/` depois de aprovação explícita.
5. Atualizar este documento quando o aprendizado for reutilizável.
6. Criar uma decisão em `DECISOES.md` somente quando a regra se tornar permanente.
7. Atualizar a ficha do personagem e o changelog quando houver impacto canônico.
