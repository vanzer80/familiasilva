# AGENTS

## Escopo

Este repositório é a fonte de verdade documental do projeto Família Silva. A organização e a rastreabilidade não autorizam a criação de conteúdo criativo. Toda informação ainda ausente deve permanecer como `A DEFINIR`.

## Fontes obrigatórias para vídeo

- A fonte executável para todo novo prompt de vídeo é [prompts/templates/TEMPLATE-MESTRE-VIDEO.md](prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- As decisões permanentes ficam em [docs/DECISOES.md](docs/DECISOES.md).
- Erros, acertos, hipóteses e soluções validadas ficam em [docs/APRENDIZADOS-DE-VIDEO.md](docs/APRENDIZADOS-DE-VIDEO.md), no adendo [docs/APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md](docs/APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md) e nos registros de [producao/](producao/).
- Observações e hipóteses de produção que ainda precisam de mais teste ficam em [docs/APRENDIZADOS-EM-VALIDACAO.md](docs/APRENDIZADOS-EM-VALIDACAO.md), a camada intermediária entre observação e regra oficial. Uma descoberta experimental entra **primeiro** ali; só depois de validada sobe para `APRENDIZADOS-DE-VIDEO.md`, `DECISOES.md` ou o template mestre. Uma IA que assumir uma nova sessão de produção deve consultar esse arquivo para recuperar as hipóteses atualmente `EM TESTE`.
- Nenhum prompt pode depender de contexto, prompt ou vídeo anterior que a ferramenta de geração não recebeu. Cada prompt deve ser autossuficiente.
- Todo pedido de criação de um novo prompt de vídeo é entregue no formato de três blocos separados — `PROMPT DO VÍDEO`, `TEXTO DE CAPA` e `DESCRIÇÃO + 5 HASHTAGS` —, conforme a seção `Formato padrão de entrega` de [prompts/templates/TEMPLATE-MESTRE-VIDEO.md](prompts/templates/TEMPLATE-MESTRE-VIDEO.md) e [DEC-022](docs/DECISOES.md#dec-022). Capa e descrição são conteúdo final de publicação, não prompts, e ficam fora do texto enviado ao gerador.

## Disciplina de validação

Aplicar obrigatoriamente a sequência aprovada em [DEC-019](docs/DECISOES.md#dec-019):

`HIPÓTESE → EM TESTE → VALIDADO → decisão/template`

- Não promover achismo, primeira impressão ou um único resultado ambíguo a regra permanente.
- Separar **fato observado** de **interpretação causal**.
- Duração do arquivo final não prova, sozinha, se a origem foi geração única, extensão, continuação ou sequência na interface.
- Quando houver dúvida sobre comportamento de ferramenta, registrar a dúvida explicitamente e testar antes de atualizar template/decisão.
- Uma correção posterior deve preservar o histórico do erro documental, mas marcar claramente qual regra vigente o substitui.
- Enquanto uma hipótese estiver `EM TESTE`, mantê-la em [docs/APRENDIZADOS-EM-VALIDACAO.md](docs/APRENDIZADOS-EM-VALIDACAO.md). Não copiá-la para `APRENDIZADOS-DE-VIDEO.md`, `DECISOES.md` ou `TEMPLATE-MESTRE-VIDEO.md` antes de `VALIDADO`. A força da evidência considera repetibilidade, diversidade de cenas/personagens, clareza de causa/efeito, ausência de explicação alternativa e impacto — não uma contagem fixa de testes. `VALIDADO` inicia a promoção mas ainda não altera o template; só `PROMOVIDO`, com destino explícito registrado, é regra oficial.
- Ao assumir uma produção em andamento, seguir a ordem de [recuperação de contexto](docs/APRENDIZADOS-EM-VALIDACAO.md#recuperação-de-contexto-por-uma-nova-ia): cânone → aprendizados em validação → `AV` relevantes → roteiro/continuidade planejada → quando já houver sequência audiovisual produzida, verificar o estado realmente realizado no último material aprovado e reconciliá-lo com o roteiro antes de continuar (hipótese [AV-008](docs/APRENDIZADOS-EM-VALIDACAO.md#av-008--continuidade-realizada-tem-precedência-operacional-sobre-roteiro-planejado), `EM TESTE`).

## Proteção de cânone

- Nunca alterar informação oficial de personagem sem autorização explícita.
- Nunca substituir silenciosamente uma decisão aprovada.
- Nunca promover um teste para material oficial automaticamente.
- Nunca tratar imagem experimental como imagem MASTER.
- Marcar materiais e decisões como `HIPÓTESE`, `EM TESTE`, `VALIDADO`, `DEFINIDO`, `APROVADO`, `APROVADO VISUALMENTE`, `APROVADO COM RESSALVAS`, `REJEITADO` ou `A DEFINIR`, conforme aplicável.
- Separar aprovação visual, vocal, narrativa e técnica. Aprovar uma dimensão não aprova automaticamente as demais.

## Personagens e versões

- Cada personagem possui um ID permanente, como `CHAR-001`.
- Cada personagem usa exclusivamente sua própria imagem MASTER ou referência visual aprovada.
- Um vídeo aprovado pode complementar o método de prompting ou rendering, mas não substitui a imagem MASTER como referência facial.
- Sr. Antônio (`CHAR-004`) e Beto (`CHAR-005`) são referências metodológicas para arquitetura de prompt e rendering, nunca referências faciais de outros personagens.
- Registrar mudanças visuais, de voz, de relação ou de continuidade no arquivo do personagem e no changelog criativo.
- Não apagar versões antigas relevantes. Preferir versionar arquivos ou registrar a alteração.

## Referências múltiplas no Gemini

Aprendizado validado na produção de S01E001 em `2026-08-29`:

- anexar todas as MASTERs dos personagens citados no prompt;
- no Gemini multi-reference, manter a ordem dos anexos alinhada à ordem dos nomes na frase de referência;
- conferir o pareamento 1:1 antes de gerar;
- se uma MASTER estiver ausente, corrigir o conjunto antes de reescrever a cena;
- essa regra de ordem foi validada para o Gemini nesta rodada e não deve ser generalizada automaticamente para outras ferramentas.

Ver [ERR-009](producao/erros/ERR-009-GEMINI-MASTERS-AUSENTES-OU-FORA-DE-ORDEM.md) / [SOL-009](producao/solucoes/SOL-009-GEMINI-MASTERS-COMPLETAS-E-ORDENADAS.md).

## Rendering da série

- O padrão canônico é `Photorealistic / Warm Cinematic Realism`.
- Evitar cartoon plano, visual infantil, pele plástica, aparência de brinquedo, proporções exageradas e deriva de rosto ou corpo.
- Não usar nomes de estúdios, franquias, obras ou artistas como atalho de estilo. Descrever materiais, iluminação, anatomia, câmera e acabamento de forma técnica.

## Continuidade audiovisual

Todo prompt de vídeo com personagens deve usar, quando aplicável:

- `Fictional Context Declaration`.
- `Character Visual Continuity`.
- `Series Rendering Style Continuity`.
- `Costume Continuity`.
- `Environment Continuity`.
- `Relationship Continuity`.
- `Speaking Continuity`.
- `Voice Continuity`.
- `Lip-Sync Continuity`.
- `Silent Character Continuity`.

Blocos não aplicáveis podem ser omitidos. Não usar linguagem de identidade de pessoa real nem instruções que afirmem que o personagem é exatamente a mesma pessoa de uma referência.

## Diálogo, emoção e voz

- Uma fala pertence exclusivamente ao personagem a que foi atribuída.
- Nunca trocar falas, aplicar a voz de um personagem a outro ou deixar um personagem completar a fala de outro.
- Personagens silenciosos não devem movimentar os lábios como se falassem.
- O lip sync deve pertencer apenas ao personagem que profere a fala correta.
- Voz ou fala experimental não se torna canônica por uma aprovação visual.
- Preferir linguagem oral brasileira natural a diálogo excessivamente escrito.
- Interjeições, pequenas repetições, hesitações e pausas podem ser usadas quando coerentes com personagem e emoção.
- A fala deve caber na duração real considerando interpretação, pausa e reação; não apenas contagem de caracteres ou leitura acelerada.
- Se a fala estiver apertada, reduzir palavras antes de sacrificar naturalidade ou aceitar corte de diálogo.

## Arquitetura narrativa

- Antes de quebrar automaticamente toda microcena em arquivo separado, avaliar se beats causalmente conectados ganham fluidez quando tratados como sequência contínua.
- O multi-beat é um princípio narrativo condicional, não uma promessa de duração da ferramenta.
- Voltar a microclipes quando duração, elenco, fala, lip sync ou deriva visual tornarem a sequência menos confiável.
- Não presumir que um arquivo de `20s` represente necessariamente uma única geração direta.
- Compressão narrativa é permitida quando preserva arco causal, conflito central, virada, resolução e payoff, sem apagar a fonte histórica.

## Fluxo de materiais de IA

Todo resultado de IA entra primeiro em `producao/testes/`. Somente aprovação explícita permite classificá-lo como aprovado. Um material aprovado pode depois ser promovido a referência oficial ou MASTER com registro de decisão.

Para cada teste, registrar ferramenta, configuração real, arquitetura, prompt ou sua situação de recuperação, referências, ordem dos anexos quando relevante, resultado, erros, correções, dimensão aprovada e impacto no cânone.

## Publicação

Quando um episódio ou asset for publicado, registrar:

- plataforma e handle oficial;
- data;
- versão/arquivo aprovado;
- metadata/hash quando disponível;
- descrição final;
- hashtags finais realmente usadas;
- diferenças entre sugestão inicial e publicação efetiva.

## Segurança de edição

- Preservar documentos e conteúdo existente.
- Não inventar características, história, idade, voz, roupa, profissão ou relações de personagens.
- Não fazer push remoto sem autorização explícita.

## Ausência de informação não autoriza invenção

Um campo `A DEFINIR`, uma pasta vazia ou uma informação ausente no Git **não** deve ser interpretada automaticamente como uma lacuna criativa livre para preencher. Antes de criar personalidade, relação, episódio, história, papel narrativo ou informação biográfica nova, verificar nesta ordem:

1. a ficha e a personalidade canônica do personagem em [personagens/oficiais/](personagens/oficiais/);
2. a matriz de relações em [personagens/relacoes/RELACOES-FAMILIARES.md](personagens/relacoes/RELACOES-FAMILIARES.md);
3. [docs/DECISOES.md](docs/DECISOES.md) e [docs/CHANGELOG-CRIATIVO.md](docs/CHANGELOG-CRIATIVO.md);
4. qualquer conteúdo marcado como `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` — isso indica que a informação **já existe fora deste repositório** e não deve ser reconstruída por suposição.

Se houver indicação de que o conteúdo já foi definido externamente, não reinventar: registrar o bloqueio e seguir apenas com o que está aprovado.
