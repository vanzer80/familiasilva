# Aprendizados finais de produção — S01E001 — 2026-08-29

Este documento consolida os aprendizados adicionais obtidos durante a produção, revisão, montagem e publicação da versão curta final de `S01E001 — A Greve da Patrícia`.

Ele **complementa** [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md) e registra também uma correção metodológica importante: informações inicialmente inferidas durante teste não devem ser promovidas a regra antes de validação objetiva.

## Correção de interpretação — LRN-015 / DEC-018

Durante os testes, foi inicialmente interpretado que o Gemini havia produzido diretamente um vídeo de aproximadamente `20 segundos` em uma única geração. Essa interpretação foi documentada cedo demais em `LRN-015` e `DEC-018`.

Posteriormente, o próprio usuário levantou a hipótese de que poderia ter usado uma sequência/continuação de vídeo em vez de uma geração única mais longa. A análise dos arquivos confirmou que existe um arquivo final de `20.010 s`, mas **o arquivo por si só não prova como a interface do Gemini o produziu**.

### Regra corrigida

- É fato validado que um dos arquivos finais usados em S01E001 tem `20.010 s` e contém dois momentos narrativos conectados.
- Continua validado que agrupar momentos causalmente ligados pode melhorar muito a fluidez narrativa.
- **Não está validado** que o Gemini, em qualquer fluxo, sempre gere `20s` diretamente em uma única chamada.
- Não distinguir geração única, extensão, continuação ou sequência sem evidência direta da operação realizada na interface.
- A duração e o mecanismo real da ferramenta devem ser validados antes de virar regra permanente.

Portanto, a parte útil do `LRN-015` é a **arquitetura narrativa multi-beat**, não uma promessa técnica de duração.

## LRN-016 — Todas as MASTERs pedidas precisam estar anexadas

### Observação

Ao tentar gerar uma cena com Marcos, Patrícia e Dudu, o Gemini retornou erro genérico porque nem todas as imagens MASTER solicitadas no prompt haviam sido anexadas.

Depois que o usuário anexou o conjunto completo, a geração funcionou.

### Regra

Em uma geração com múltiplos personagens:

1. identificar todos os personagens citados na frase de referências;
2. anexar a MASTER V02 PHOTOREALISTIC de **cada um**, sem omissões;
3. conferir o conjunto antes de gerar.

### Limite

Essa causa foi validada para o erro específico reproduzido nesta rodada. Nem todo erro genérico do Gemini deve ser automaticamente atribuído a referência ausente.

**Evidência:** [ERR-009](../producao/erros/ERR-009-GEMINI-MASTERS-AUSENTES-OU-FORA-DE-ORDEM.md) / [SOL-009](../producao/solucoes/SOL-009-GEMINI-MASTERS-COMPLETAS-E-ORDENADAS.md).

## LRN-017 — Ordem das MASTERs deve acompanhar a ordem dos nomes no prompt no Gemini

### Observação

O usuário verificou que, no Gemini, anexar referências fora da sequência em que os personagens são apresentados no prompt pode levar a associações incorretas, incluindo inversão de fala e papel.

### Regra operacional validada nesta rodada

Se o prompt começa com:

`Use the uploaded master images of Carol, Marcos, Patrícia and Dudu...`

anexar as MASTERs na sequência:

1. Carol;
2. Marcos;
3. Patrícia;
4. Dudu.

A ordem dos nomes e a ordem dos arquivos devem formar um pareamento 1:1 verificável antes da geração.

### Escopo

Esta é uma regra operacional validada para o Gemini nesta produção. Não generalizar automaticamente para Flow, Veo ou outra interface sem teste equivalente.

## LRN-018 — Diálogo emocional precisa caber na janela real do clipe

### Observação

Um teste com duas cenas e falas longas em um arquivo de aproximadamente `10.005 s` cortou parte do diálogo. O problema não era apenas conteúdo textual; havia mais fala, ação e reação do que cabia confortavelmente na duração efetiva.

### Regra

- Escrever fala como linguagem oral, com emoção, pausa e respiração reais.
- Não usar apenas contagem de caracteres como critério de duração.
- Uma fala que cabe tecnicamente quando lida rápido pode não caber quando interpretada com emoção.
- Quando uma cena depende de hesitação, pausa, reação ou pedido de desculpas, reduzir a quantidade de palavras para preservar atuação natural.

### Exemplo validado de ajuste

A fala emocional de Marcos foi enxugada para:

`Patrícia... eu achei que tava ajudando, sabe? Mas só agora percebi que fazia tempo que eu nem perguntava como tu tava. Me desculpa.`

A versão gerada foi aprovada pelo usuário como excelente.

## LRN-019 — Linguagem falada é superior a diálogo excessivamente escrito

Nos testes finais de S01E001, as falas melhoraram quando foram reescritas para soar como conversa real de uma família brasileira, incluindo:

- repetição espontânea (`Mãe, mãe...` / `Chega! Chega, gente!`);
- interjeições (`Tá...`, `Pronto!`, `sabe?`);
- pequenas pausas;
- mudança de energia dentro da própria frase;
- vergonha, irritação, urgência, ironia ou afeto coerentes com o personagem;
- frases ligeiramente imperfeitas, como pessoas realmente falam.

A direção de atuação deve explicitar a emoção sem transformar a cena em interpretação teatral exagerada.

## LRN-020 — A duração deve servir ao beat, não o contrário

A versão final publicada usa durações diferentes:

- primeiro arquivo: `20.010 s`;
- quatro arquivos seguintes: `10.005 s` cada;
- montagem final: `60.051333 s`.

Isso validou uma regra de edição importante: **não impor a mesma duração a todos os momentos apenas por uniformidade**. O beat narrativo, a quantidade de fala e o tempo de reação devem orientar a escolha da duração/configuração disponível.

Isso não define `20s` ou `10s` como duração canônica da série.

## LRN-021 — Compressão narrativa pode melhorar o episódio sem apagar a fonte histórica

A fonte histórica de S01E001 contém 12 cenas e 29 clipes. A versão final publicada foi condensada para cinco arquivos, com aproximadamente um minuto total.

O resultado foi aprovado porque preservou um arco causal claro:

`dependência da Patrícia → greve → consequência → solução prática insuficiente → percepção emocional → pedido de desculpas → pequeno aprendizado do Dudu`.

Nem todos os personagens e subtramas da fonte histórica precisaram aparecer nesta versão curta.

### Regra

Uma adaptação curta pode remover subtramas quando isso:

- melhora foco;
- preserva causa e consequência;
- mantém o conflito central compreensível;
- produz começo, desenvolvimento, virada, resolução e payoff final.

A fonte histórica permanece preservada; a versão publicada é uma adaptação aprovada, não uma reescrita retroativa da fonte.

## LRN-022 — O payoff silencioso pode ser mais forte que uma fala adicional

No fechamento, Dudu pergunta automaticamente pelo carregador. Patrícia e Marcos apenas olham para ele. Dudu percebe sozinho e corrige o comportamento.

A ausência de resposta verbal dos pais permitiu que a comédia viesse de:

- reconhecimento;
- olhar;
- pausa;
- constrangimento;
- autocorreção.

Regra reutilizável: quando a informação já foi estabelecida pelo episódio, não explicar novamente em diálogo se uma reação silenciosa consegue entregar o payoff.

## LRN-023 — Não registrar hipótese como regra antes de validar

Este é o principal aprendizado metodológico desta rodada.

O registro inicial sobre `20 segundos em uma geração` foi feito antes de a operação estar suficientemente comprovada. O usuário identificou a fragilidade e determinou que novos upgrades sejam testados antes de serem promovidos a regra documental.

### Nova disciplina de documentação

1. ideia ou suspeita → `HIPÓTESE`;
2. primeiro resultado positivo → `EM TESTE`;
3. reprodução/inspeção objetiva → `VALIDADO`;
4. somente depois, se reutilizável e desejado → decisão permanente/template.

Quando houver dúvida sobre interface, duração, extensão, sequência ou comportamento interno de uma ferramenta, registrar exatamente o que foi observado e separar isso da interpretação de como a ferramenta chegou ao resultado.

## Evidência final

A versão final publicada está registrada em [APROVACAO-S01E001-VERSAO-FINAL-PUBLICADA-001.md](../producao/aprovados/APROVACAO-S01E001-VERSAO-FINAL-PUBLICADA-001.md).
