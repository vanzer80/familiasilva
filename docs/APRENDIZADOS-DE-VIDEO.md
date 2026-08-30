# Aprendizados de Vídeo

Este documento consolida o que foi aprendido nos testes audiovisuais da Família Silva. Ele não substitui as decisões formais nem o template mestre:

- [DECISOES.md](DECISOES.md) define o que é permanente e aprovado.
- [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md) define como construir cada novo prompt.
- [producao/](../producao/) preserva a evidência de testes, erros, soluções, aprovações e rejeições.
- [APRENDIZADOS-EM-VALIDACAO.md](APRENDIZADOS-EM-VALIDACAO.md) é a camada anterior a este documento: guarda as observações e hipóteses de produção ainda `EM TESTE`. Um aprendizado só recebe um `LRN` aqui **depois** de ser marcado como `VALIDADO` lá.

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
- **Validação adicional (`2026-08-28`):** as sete MASTERs V02 PHOTOREALISTIC foram usadas para gerar vídeos individuais de apresentação no Google Flow, um por personagem. As sete gerações apresentaram o rendering `Photorealistic / Warm Cinematic Realism` esperado, sem cartoon/3D/CGI, com identidade visual considerada consistente com a respectiva MASTER V02; o usuário aprovou as sete. Três delas (Dudu, Sr. Antônio, Beto) precisaram de reformulação de compliance antes de gerar com sucesso — não por falha de rendering ou de identidade, mas por um bloqueio de possível "pessoa famosa" (ver [LRN-014](#lrn-014--falso-positivo-de-pessoa-famosa-no-flow-para-personagem-ficcional)).
- **Status:** `VALIDADO` pela [DEC-015](DECISOES.md#dec-015).

### LRN-014 — Falso positivo de "pessoa famosa" no Flow para personagem ficcional

- **Observação:** durante a validação em vídeo das MASTERs V02 PHOTOREALISTIC (`2026-08-28`), o Flow bloqueou Dudu, Sr. Antônio e Beto com mensagem de possível violação de política sobre pessoas famosas, mesmo sendo personagens ficcionais originais com MASTER própria. Marcos, Dona Célia, Patrícia e Carol não sofreram esse bloqueio na mesma rodada, usando o mesmo tipo de referência.
- **Causa:** desconhecida. A causa interna do classificador do Flow não é observável a partir deste repositório; qualquer explicação é hipótese, não fato.
- **Solução (fallback validado):** reformular o contexto de compliance em linguagem simples e factual — personagem ficcional original, imagem de referência pertencente ao projeto, sem intenção de retratar pessoa real — mantendo o requisito de live-action photorealistic e evitando linguagem biométrica rígida (`EXACTLY the same person`, `absolute source of truth for identity`, `biometric identity`, `face cloning`) ou listas longas de negative constraints. Ver [ERR-008](../producao/erros/ERR-008-FLOW-FALSO-POSITIVO-PESSOA-FAMOSA.md) e [SOL-008](../producao/solucoes/SOL-008-CONTEXTO-FICCIONAL-COMPLIANCE-FLOW.md).
- **Limite:** usar apenas quando esse bloqueio específico ocorrer.
- **Status:** `VALIDADO` como fallback nos três casos desta rodada.

### LRN-015 — Arquitetura narrativa multi-beat para microcenas encadeadas

- **Observação:** em `2026-08-29`, testes de S01E001 mostraram que microcenas causalmente conectadas podem ganhar fluidez quando tratadas como uma sequência narrativa contínua. O primeiro arquivo final auditado contém dois momentos conectados e tem `20.010 s`; o usuário avaliou a transição como muito mais fluida.
- **Correção metodológica:** o registro inicial inferiu cedo demais que `20 segundos` eram uma capacidade direta de uma única geração do Gemini. Depois, o usuário levantou a possibilidade de ter usado sequência/continuação. O binário confirma sua duração, mas **não permite determinar sozinho se a origem foi geração única, extensão, continuação ou sequência na interface**.
- **Solução:** antes de dividir automaticamente o roteiro em um vídeo por microcena, avaliar se duas ou mais microcenas podem ser organizadas como beats de uma sequência contínua quando os momentos forem causal ou emocionalmente encadeados, compartilhem ambiente/bloco temporal/figurino e tenham atribuição de fala controlável.
- **Regra de fala:** `LRN-011` continua válido. A exclusividade de fala pode ser aplicada por beat.
- **Duração:** não transformar `20s` em regra universal nem assumir o mecanismo da ferramenta. Validar a duração/configuração e a operação real usadas.
- **Fallback:** voltar a microclipes quando houver mudança grande de ambiente/tempo/figurino, excesso de personagens ou ações, risco alto de troca de fala/voz/lip sync, deriva visual/narrativa, limitação da plataforma ou resultado inferior.
- **Status:** `VALIDADO COMO PRINCÍPIO NARRATIVO CONDICIONAL`; correção formal em [DEC-018](DECISOES.md#dec-018) / [DEC-019](DECISOES.md#dec-019).

### LRN-016 — Todas as MASTERs citadas precisam estar anexadas

- **Observação:** uma geração no Gemini retornou erro genérico quando nem todas as MASTERs dos personagens citados estavam anexadas.
- **Validação:** após anexar o conjunto completo, a geração funcionou.
- **Solução:** conferir todos os personagens citados e anexar a MASTER V02 de cada um, sem omissões.
- **Limite:** não concluir que todo erro genérico do Gemini tem essa causa.
- **Evidência:** [ERR-009](../producao/erros/ERR-009-GEMINI-MASTERS-AUSENTES-OU-FORA-DE-ORDEM.md) / [SOL-009](../producao/solucoes/SOL-009-GEMINI-MASTERS-COMPLETAS-E-ORDENADAS.md).
- **Status:** `VALIDADO NESTA RODADA`.

### LRN-017 — Ordem das MASTERs deve acompanhar a ordem dos nomes no prompt no Gemini

- **Observação:** o usuário verificou que referências anexadas fora da sequência dos nomes no prompt podem levar o Gemini a inverter associação, papel ou fala.
- **Solução:** no Gemini, alinhar 1:1 a ordem da frase de referências e a ordem dos anexos. Exemplo: `Carol, Marcos, Patrícia and Dudu` → anexar Carol, Marcos, Patrícia, Dudu nessa sequência.
- **Escopo:** regra operacional específica do Gemini nesta rodada; não generalizar automaticamente para outras ferramentas.
- **Status:** `VALIDADO NESTA RODADA` pela [DEC-019](DECISOES.md#dec-019).

### LRN-018 — Diálogo emocional precisa caber na janela real do clipe

- **Observação:** um teste com conteúdo demais em aproximadamente `10.005 s` cortou falas. Leitura rápida não é medida suficiente porque emoção, pausa e reação consomem tempo.
- **Solução:** reduzir palavras para preservar interpretação, respiração e reação. Não acelerar artificialmente a fala para “caber”.
- **Exemplo aprovado:** `Patrícia... eu achei que tava ajudando, sabe? Mas só agora percebi que fazia tempo que eu nem perguntava como tu tava. Me desculpa.`
- **Status:** `VALIDADO` na versão final de S01E001.

### LRN-019 — Linguagem falada e emoção específica

- **Observação:** as falas finais melhoraram quando foram reescritas como conversa real de família brasileira, com interjeições, repetições, pequenas pausas, hesitações e emoção específica.
- **Aplicação:** permitir formulações como `Mãe, mãe...`, `Chega! Chega, gente!`, `Tá...`, `Pronto!`, `sabe?` quando coerentes com personagem e momento.
- **Direção de atuação:** explicitar urgência, irritação, vergonha, afeto, ironia ou arrependimento sem melodrama ou teatralidade exagerada.
- **Status:** `VALIDADO` em S01E001.

### LRN-020 — A duração deve servir ao beat

- **Observação:** a versão final publicada usa um arquivo de `20.010 s` e quatro de `10.005 s`, totalizando montagem de `60.051333 s`.
- **Solução:** não impor uma duração única apenas por uniformidade; escolher a configuração disponível conforme quantidade de fala, ação, pausa e reação.
- **Limite:** essas durações não se tornam padrão canônico da série.
- **Status:** `VALIDADO` pela versão final publicada de S01E001.

### LRN-021 — Compressão narrativa pode melhorar foco sem apagar a fonte histórica

- **Observação:** a fonte histórica tem 12 cenas/29 clipes; a versão publicada foi condensada para cinco arquivos e aproximadamente um minuto.
- **Arco preservado:** `dependência da Patrícia → greve → consequência → solução prática insuficiente → percepção emocional → pedido de desculpas → pequeno aprendizado do Dudu`.
- **Solução:** permitir remoção de subtramas quando a versão curta preserva causa e consequência, conflito central, virada, resolução e payoff.
- **Preservação:** a fonte histórica permanece íntegra; a versão publicada é adaptação aprovada, não reescrita retroativa.
- **Status:** `VALIDADO` pela [DEC-020](DECISOES.md#dec-020).

### LRN-022 — Payoff silencioso pode ser mais forte que fala explicativa

- **Observação:** no final de S01E001, Patrícia e Marcos apenas olham para Dudu; ele percebe sozinho que repetiu o padrão e decide procurar o carregador.
- **Solução:** quando o episódio já estabeleceu a informação, preferir olhar, pausa, constrangimento e autocorreção a uma fala explicativa redundante.
- **Status:** `VALIDADO` como recurso narrativo na versão publicada.

### LRN-023 — Não registrar hipótese como regra antes de validar

- **Observação:** a interpretação inicial sobre `20s em uma geração` foi promovida cedo demais. O usuário identificou a fragilidade e determinou que novos upgrades sejam validados antes de entrar como regra.
- **Disciplina:** `HIPÓTESE → EM TESTE → VALIDADO → decisão/template`.
- **Aplicação:** separar sempre fato observado de interpretação causal, especialmente em comportamento de interface, duração, extensão, sequência e classificadores de geração.
- **Status:** `APROVADO` pela [DEC-019](DECISOES.md#dec-019).

Detalhamento adicional desta rodada: [APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md](APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md).

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

Observações e hipóteses novas nascem em [APRENDIZADOS-EM-VALIDACAO.md](APRENDIZADOS-EM-VALIDACAO.md) (entradas `AV-0XX`) e só chegam a este documento como `LRN` depois de `VALIDADO`. O fluxo abaixo continua válido e é a versão detalhada desse mesmo caminho.

1. Registrar ideia ou suspeita como `HIPÓTESE`.
2. Criar o registro em `producao/testes/` antes da geração ou avaliação quando aplicável.
3. Registrar cada defeito em `producao/erros/`, distinguindo fato de hipótese.
4. Registrar a correção em `producao/solucoes/` e vinculá-la ao erro.
5. Um primeiro resultado positivo permanece `EM TESTE` se ainda houver dúvida sobre causa ou mecanismo.
6. Só promover uma conclusão para `VALIDADO` após reprodução, inspeção objetiva ou confirmação suficiente.
7. Só mover material para `producao/aprovados/` depois de aprovação explícita.
8. Atualizar este documento quando o aprendizado for reutilizável.
9. Criar uma decisão em `DECISOES.md` somente quando a regra se tornar permanente.
10. Atualizar ficha, continuidade, changelog e publicação quando houver impacto canônico ou de produção.
