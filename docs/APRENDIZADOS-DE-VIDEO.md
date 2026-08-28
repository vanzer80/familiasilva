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

### LRN-010 — Não copiar rótulos técnicos para o prompt final

- **Observação:** Character IDs, nomes técnicos de clipe (por exemplo `Clip 1C`), cabeçalhos administrativos e metadados do pipeline pertencem à documentação de produção, não ao texto enviado ao gerador; se copiados para o prompt, arriscam aparecer como texto visível no vídeo.
- **Solução:** manter esses identificadores apenas nos registros em `producao/` e nos nomes de arquivo; o prompt operacional deve conter somente linguagem natural e instruções de continuidade.
- **Status:** `VALIDADO` como regra de composição de prompt.

### LRN-011 — Um falante principal quando há risco de troca de fala

- **Observação:** cenas com mais de um personagem aumentam o risco de o modelo trocar a fala, a voz ou o lip sync entre eles.
- **Solução:** quando esse risco existir, priorizar apenas um personagem falando por geração, mantendo o(s) demais explicitamente silencioso(s) via `Silent Character Continuity`, combinado com `Speaking Continuity`, `Voice Continuity` e `Lip-Sync Continuity`.
- **Limite:** é uma heurística de mitigação de risco, não uma regra obrigatória para toda cena com múltiplos personagens.
- **Status:** `VALIDADO` como heurística de composição de prompt.

### LRN-012 — Simplificação controlada

- **Observação:** mais restrições e negative constraints não produzem automaticamente um resultado melhor; em alguns casos um prompt mais enxuto e semanticamente claro supera um prompt com dezenas de restrições.
- **Solução:** manter apenas os blocos e negative constraints aplicáveis e proporcionais ao problema real da cena; blocos sem utilidade podem ser omitidos, conforme já previsto na filosofia do [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- **Status:** `VALIDADO` como princípio de composição; não substitui os locks obrigatórios (Speaking, Voice, Lip-Sync, Silent Character, Relationship).

### LRN-013 — Referências fotorrealistas reduzem instabilidade de conversão para live-action

- **Observação:** as MASTERs originais (`V01`) tinham visual estilizado/3D. Historicamente, essas mesmas referências conseguiram, em alguns casos, gerar vídeos fotorrealistas no Flow — não é verdade que uma referência estilizada/3D nunca consiga produzir fotorrealismo. Porém, em testes recentes, com diferentes arquiteturas de prompt e configurações/modelos do Flow, ocorreram repetidamente resultados em 3D/cartoon mesmo com prompts solicitando explicitamente `Photorealistic / Warm Cinematic Realism`. O comportamento não se mostrou suficientemente estável para garantir reprodução consistente do live-action a partir de referências estilizadas.
- **Não registrar como regra absoluta:** "uma imagem 3D nunca consegue gerar vídeo fotorealista" é falso segundo os testes históricos e não deve ser usado como justificativa.
- **Solução:** criar e adotar MASTERs `V02 PHOTOREALISTIC` para os sete personagens, alinhando a referência visual de entrada ao rendering desejado dos vídeos. Referências estilizadas/3D podem gerar fotorrealismo em alguns casos, mas demonstraram comportamento instável; MASTERs fotorrealistas reduzem o conflito entre referência visual e estilo de rendering desejado e passam a ser o padrão recomendado (`CURRENT CANON`). As V01 permanecem preservadas como histórico e como referência metodológica de identidade, mas não devem ser escolhidas automaticamente para novas gerações.
- **Validação adicional (`2026-08-28`):** as sete MASTERs V02 PHOTOREALISTIC foram usadas para gerar vídeos individuais de apresentação no Google Flow, um por personagem. As sete gerações apresentaram o rendering `Photorealistic / Warm Cinematic Realism` esperado, sem cartoon/3D/CGI, com identidade visual considerada consistente com a respectiva MASTER V02; o usuário aprovou as sete. Três delas (Dudu, Sr. Antônio, Beto) precisaram de reformulação de compliance antes de gerar com sucesso — não por falha de rendering ou de identidade, mas por um bloqueio de possível "pessoa famosa" (ver [LRN-014](#lrn-014--falso-positivo-de-pessoa-famosa-no-flow-para-personagem-ficcional)). Isso fortalece, mas não substitui, a conclusão já registrada: MASTER V02 PHOTOREALISTIC demonstrou comportamento adequado e consistente nesta nova rodada de testes e permanece o padrão recomendado/`CURRENT CANON`. Não se registra a afirmação absoluta de que MASTER V01/3D nunca pode gerar fotorrealismo — o próprio histórico deste repositório mostra que isso já ocorreu.
- **Status:** `VALIDADO` pela [DEC-015](DECISOES.md#dec-015).

### LRN-014 — Falso positivo de "pessoa famosa" no Flow para personagem ficcional

- **Observação:** durante a validação em vídeo das MASTERs V02 PHOTOREALISTIC (`2026-08-28`), o Flow bloqueou Dudu, Sr. Antônio e Beto com mensagem de possível violação de política sobre pessoas famosas, mesmo sendo personagens ficcionais originais com MASTER própria. Marcos, Dona Célia, Patrícia e Carol não sofreram esse bloqueio na mesma rodada, usando o mesmo tipo de referência (MASTER V02 PHOTOREALISTIC).
- **Causa:** desconhecida. A causa interna do classificador do Flow não é observável a partir deste repositório; qualquer explicação (por exemplo, semelhança aparente com pessoa famosa) é hipótese, não fato, e não deve ser registrada como tal em nenhum documento.
- **Solução (fallback validado):** reformular o contexto de compliance em linguagem simples e factual — personagem ficcional original, imagem de referência pertencente ao projeto, sem intenção de retratar pessoa real — mantendo, sem enfraquecer, o requisito de live-action photorealistic e evitando linguagem biométrica rígida (`EXACTLY the same person`, `absolute source of truth for identity`, `biometric identity`, `face cloning`) ou listas longas de negative constraints. Ver [ERR-008](../producao/erros/ERR-008-FLOW-FALSO-POSITIVO-PESSOA-FAMOSA.md) e [SOL-008](../producao/solucoes/SOL-008-CONTEXTO-FICCIONAL-COMPLIANCE-FLOW.md).
- **Limite:** este fallback deve ser usado apenas quando esse bloqueio específico de "pessoa famosa" ocorrer. Não é uma obrigação universal para todo prompt; prompts sem esse bloqueio continuam seguindo o template enxuto padrão de [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- **Status:** `VALIDADO` como procedimento de fallback nos três casos desta rodada (`2026-08-28`); a causa interna do classificador do Flow permanece desconhecida.

## Estado dos casos conhecidos

**Nota de reconciliação (`2026-08-28`, [DEC-013](DECISOES.md#dec-013)):** a coluna "Estado visual registrado" abaixo preserva o rótulo original de cada teste, como aprendizado histórico. O **status canônico vigente** de Marcos, Dona Célia, Patrícia, Sr. Antônio, Beto e Dudu foi reconciliado para aprovação plena de canon visual (ver as fichas em `personagens/oficiais/` e a tabela em [CONTINUIDADE.md](CONTINUIDADE.md)); os aprendizados e limites técnicos desta tabela continuam válidos e devem orientar novos prompts, mas não representam mais o status de aprovação atual.

| Personagem | Estado visual registrado (histórico, na data do teste) | Aprendizado preservado | Limites |
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
