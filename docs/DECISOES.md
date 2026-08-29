# Decisões

Este documento registra decisões formais do projeto. Não registrar ideias soltas, hipóteses ou resultados ainda não aprovados como decisão.

## DEC-001

- **Data:** `2026-08-28`
- **Decisão:** adotar como canônicas as sete personalidades revisadas e a matriz cruzada de relações de Marcos, Patrícia, Carol, Dudu, Dona Célia, Beto e Sr. Antônio.
- **Motivo:** eliminar registros provisórios e assimetrias entre documentos criados em momentos diferentes, preservando o núcleo de personalidade já aprovado.
- **Impacto:** as personalidades, formas de falar, mecanismos de humor, limites de comportamento e relações registradas passam a orientar roteiros e continuidade. Nenhuma decisão visual, imagem MASTER, aparência, figurino, rendering, voz ou Character ID ausente é alterada por esta decisão.
- **Status:** `APROVADO`
- **Evidência:** [RELATORIO-AUDITORIA-CANONICA-PERSONALIDADES-2026-08-28.md](auditorias/RELATORIO-AUDITORIA-CANONICA-PERSONALIDADES-2026-08-28.md)

## DEC-002

- **Data:** `2026-08-28`
- **Decisão:** aprovar e registrar como permanentes os Character IDs `CHAR-001` Marcos Silva, `CHAR-002` Dona Célia, `CHAR-003` Patrícia Silva, `CHAR-004` Antônio Silva, `CHAR-005` Beto, `CHAR-006` Carol Silva e `CHAR-007` Dudu Silva.
- **Motivo:** eliminar as pendências de identificação do elenco inicial e estabelecer uma fonte de verdade única para fichas, personalidades, continuidade e materiais futuros.
- **Impacto:** ficam criadas as cinco fichas-base que faltavam e ratificadas as duas já existentes. Beto permanece oficialmente apenas `Beto`. Antônio Silva é conhecido como `Sr. Antônio`; seu sobrenome não o torna integrante oficial da Família Silva. Nenhuma aparência, imagem MASTER, figurino, rendering, voz, idade ou profissão é aprovada por esta decisão.
- **Status:** `APROVADO`
- **Evidência:** [cadastro canônico de personagens](../personagens/README.md)

## DEC-003

- **Data:** `2026-08-28`
- **Decisão:** adotar `Photorealistic / Warm Cinematic Realism` como padrão canônico de rendering da série Família Silva.
- **Motivo:** os testes mostraram maior coerência e continuidade no realismo cinematográfico aquecido do que no cartoon ou em descrições genéricas de realismo estilizado.
- **Impacto:** todo novo prompt visual ou audiovisual deve usar materiais fisicamente plausíveis, textura natural de pele, anatomia e proporções críveis, iluminação cinematográfica quente e profundidade de campo realista. Devem ser evitados cartoon plano, aparência infantil, pele plástica, visual de brinquedo e proporções exageradas. A terminologia anterior `stylized realism` fica superada quando contradizer esta decisão.
- **Status:** `APROVADO`
- **Evidência:** [aprendizados de vídeo](APRENDIZADOS-DE-VIDEO.md) e [padrão aprovado](../producao/aprovados/PADRAO-RENDERING-VIDEO-001.md)

## DEC-004

- **Data:** `2026-08-28`
- **Decisão:** tornar [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md) a única fonte executável para a arquitetura dos novos prompts de vídeo.
- **Motivo:** o Google Flow/Veo não recebe automaticamente prompts ou vídeos anteriores; cada geração precisa carregar todo o contexto necessário e as travas de continuidade corretas.
- **Impacto:** os prompts devem ser autossuficientes e usar, quando aplicáveis, `Fictional Context Declaration`, `Character Visual Continuity`, `Series Rendering Style Continuity`, `Costume Continuity`, `Environment Continuity`, `Relationship Continuity`, `Speaking Continuity`, `Voice Continuity`, `Lip-Sync Continuity` e `Silent Character Continuity`. A linguagem antiga de identity lock e afirmações de pessoa real não deve ser usada em instruções ativas.
- **Status:** `APROVADO`
- **Evidência:** [template mestre](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md) e [soluções validadas](../producao/solucoes/README.md)

## DEC-005

- **Data:** `2026-08-28`
- **Decisão:** manter a imagem MASTER própria de cada personagem como referência facial primária e classificar vídeos aprovados apenas como referências complementares da dimensão explicitamente aprovada.
- **Motivo:** usar outro personagem ou um vídeo anterior como referência facial provoca deriva visual e pode misturar características entre personagens.
- **Impacto:** Sr. Antônio (`CHAR-004`) e Beto (`CHAR-005`) podem orientar arquitetura de prompt e rendering, mas nunca o rosto de outro personagem. Um teste visualmente aprovado não canoniza automaticamente fala, voz, personalidade, atuação ou dinâmica narrativa.
- **Status:** `APROVADO`
- **Evidência:** [referências metodológicas](../producao/aprovados/REFERENCIAS-METODOLOGICAS-ANTONIO-BETO.md) e [aprovação visual de Carol](../producao/aprovados/APROVACAO-VISUAL-CAROL-CHAR-006-001.md)

## DEC-006

- **Data:** `2026-08-28`
- **Decisão:** registrar o primeiro teste de vídeo de Carol Silva (`CHAR-006`) como `APROVADO VISUALMENTE` no padrão canônico de rendering.
- **Motivo:** o teste validou `Character Visual Continuity` e compatibilidade com `Photorealistic / Warm Cinematic Realism`.
- **Impacto:** a aprovação vale somente para a dimensão visual. A fala usada no teste, a voz, a interpretação vocal e a dinâmica narrativa permanecem experimentais e não canônicas. A imagem MASTER de Carol continua sendo a referência facial primária.
- **Status:** `APROVADO`
- **Evidência:** [registro do teste](../producao/testes/TESTE-VIDEO-CAROL-CHAR-006-001.md)

## Nota de reconciliação — `2026-08-28`

As decisões DEC-007 a DEC-012 abaixo foram originalmente registradas, na mesma data, sob os identificadores `DEC-001` a `DEC-006` em um checkpoint local (`e954c01`) que nunca havia sido enviado a este repositório remoto quando DEC-001 a DEC-006 acima foram publicadas. As duas séries foram produzidas de forma independente e usaram a mesma numeração para decisões diferentes. Esta renumeração resolve apenas a colisão de identificadores; não representa mudança cronológica, de conteúdo ou de autoria em relação ao registro original. DEC-013 e DEC-014 documentam a própria reconciliação.

## DEC-007

- **Data:** `2026-08-27` (renumerado de `DEC-001` do checkpoint local em `2026-08-28`)
- **Decisão:** adotar `Visual Continuity` como padrão visual para prompts de vídeo de personagens fictícios originais.
- **Motivo:** reduzir falsos positivos nos filtros de geração relacionados a reprodução de pessoas famosas ou reais, sem perder a consistência visual dos personagens fictícios.
- **Impacto:** substitui `CHARACTER IDENTITY LOCK` como terminologia padrão nos prompts. Mantém Speaking Lock, Voice Lock, Lip-Sync Lock, Silent Character Lock, Relationship Lock e continuidade física e visual quando aplicáveis. Esta terminologia foi posteriormente absorvida e refinada pelas continuidades nomeadas em `personagens/regras/` (ver DEC-004).
- **Status:** `APROVADO / HISTÓRICO — terminologia consolidada em personagens/regras/`

## DEC-008

- **Data:** `2026-08-27` (renumerado de `DEC-002` do checkpoint local em `2026-08-28`)
- **Decisão:** Família Silva adota Stylized Cinematic Realism como estilo canônico de renderização da série.
- **Motivo:** o vídeo de Sr. Antônio (`CHAR-004`) atingiu acabamento visual superior e passou a orientar o nível de realismo, textura, iluminação, materiais, profundidade de campo e equilíbrio entre cartoon e realismo.
- **Status:** `SUPERADO — ver DEC-009 e DEC-003`. Mantido apenas como histórico; não deve orientar rendering, prompts ou novas gerações.

## DEC-009

- **Data:** `2026-08-27` (renumerado de `DEC-003` do checkpoint local em `2026-08-28`)
- **Decisão:** `CHAR-005` — Beto é aprovado como canon visual em vídeo. Prompts de vídeo passam a usar `Photorealistic / Warm Cinematic Realism` como direção operacional de rendering.
- **Motivo:** o vídeo final de Beto confirmou que a estrutura usada no vídeo aprovado de Sr. Antônio produz aparência humana mais natural, materiais realistas, proporções faciais menos caricatas, iluminação cinematográfica e estabilidade visual sem o aspecto excessivamente cartoon da tentativa anterior.
- **Impacto:** substitui operacionalmente a terminologia de rendering de `DEC-008`, sem apagar seu registro histórico. Confirma e antecede o mesmo padrão formalizado em `DEC-003`.
- **Status:** `APROVADO` — consistente com `DEC-003`.
- **Evidência:** [referências metodológicas](../producao/aprovados/REFERENCIAS-METODOLOGICAS-ANTONIO-BETO.md)

## DEC-010

- **Data:** `2026-08-27` (renumerado de `DEC-004` do checkpoint local em `2026-08-28`)
- **Decisão:** `CHAR-006` — Carol Silva tem primeiro teste de vídeo `APROVADO VISUALMENTE`.
- **Motivo:** o teste demonstrou estabilidade visual, consistência facial e corporal, cabelo, idade aparente, iluminação, rendering e integração com `Photorealistic / Warm Cinematic Realism`.
- **Limites de cânone:** a imagem MASTER de Carol permanece a referência facial primária. Diálogo experimental, dinâmica sugerida, personalidade inferida e voz usada no teste não se tornam cânone. Não há Voice Master formalizado para Carol.
- **Status:** `APROVADO — decisão confirmatória, já formalizada em DEC-006`.

## DEC-011

- **Data:** `2026-08-27` (renumerado de `DEC-005` do checkpoint local em `2026-08-28`)
- **Decisão:** `CHAR-007` — Dudu Silva é `APROVADO / CANON VISUAL` em vídeo.
- **Motivo:** o resultado visual demonstrou rosto consistente, roupa e silhueta estáveis, ambiente doméstico coerente, performance compatível com comédia familiar e alinhamento com `Photorealistic / Warm Cinematic Realism`.
- **Ajuste metodológico:** para intenção dramática de injustiçado ou de questionamento sobre culpa, evitar sorriso excessivamente simpático.
- **Status:** `APROVADO / CANON VISUAL — status confirmado por DEC-013, que resolve a divergência com o registro em ERR-006/TESTE-REFERENCIA-DUDU-CHAR-007-001.md`.

## DEC-012

- **Data:** `2026-08-27` (renumerado de `DEC-006` do checkpoint local em `2026-08-28`)
- **Decisão:** aprovar os vídeos de validação de `CHAR-001` — Marcos Silva, `CHAR-002` — Dona Célia e `CHAR-003` — Patrícia Silva como `CANON VISUAL PARA RENDERING DE VÍDEO` no padrão `Photorealistic / Warm Cinematic Realism`.
- **Motivo:** os resultados demonstraram continuidade facial, corporal, de figurino e ambiente, rendering natural, iluminação cinematográfica quente e atuação contida compatíveis com o padrão vigente da série.
- **Registro técnico de Patrícia:** vídeo aprovado com aproximadamente `6 segundos`, `720 x 1280`, `24 fps`, formato vertical e áudio presente; duração escolhida deliberadamente pelo usuário, não representando limitação do Flow.
- **Restrições:** não usar pessoas reais, marcas, estúdios, franquias ou personagens externos como referência visual canônica ou facial.
- **Status:** `APROVADO / CANON VISUAL PARA RENDERING DE VÍDEO — status confirmado por DEC-013`.

## DEC-013

- **Data:** `2026-08-28`
- **Decisão:** em caso de divergência entre uma aprovação de vídeo explicitamente registrada após análise de teste real (DEC-007 a DEC-012) e uma reclassificação documental posterior sem nova evidência de produção (DEC-002 e DEC-005 desta série, e os registros `APROVADO COM RESSALVAS` / `AJUSTE VISUAL NECESSÁRIO` nas fichas e em `producao/testes/`), prevalece a aprovação baseada em evidência de produção real. Especificamente, `CHAR-001`, `CHAR-002`, `CHAR-003`, `CHAR-004`, `CHAR-005` e `CHAR-007` mantêm o status pleno de aprovação visual de DEC-009, DEC-011 e DEC-012, e não o rótulo `APROVADO COM RESSALVAS` / `AJUSTE VISUAL NECESSÁRIO` atribuído por DEC-002/DEC-005.
- **Motivo:** decisão explícita do usuário nesta reconciliação (`2026-08-28`), fundamentada no princípio de que uma reauditoria documental não deve, por si só, revogar uma aprovação já concedida com base em produção real, na ausência de evidência objetiva e específica de revogação.
- **Impacto:** `ERR-002-DERIVA-VISUAL-CORPORAL.md` (Marcos) e `ERR-006-REFERENCIA-DUDU-NAO-NEUTRA.md` / `TESTE-REFERENCIA-DUDU-CHAR-007-001.md` (Dudu) permanecem integralmente preservados como aprendizado de produção e devem orientar os próximos prompts, mas deixam de ser lidos como revogação do status canônico. `CHAR-006` (Carol) não é afetada, pois DEC-006 e DEC-010 já concordam em `APROVADO VISUALMENTE`.
- **Status:** `APROVADO`
- **Evidência:** tabela de reconciliação apresentada nesta sessão; `ERR-002-DERIVA-VISUAL-CORPORAL.md`; `ERR-006-REFERENCIA-DUDU-NAO-NEUTRA.md`

## DEC-014

- **Data:** `2026-08-28`
- **Decisão:** ingerir neste repositório as sete imagens MASTER e o `MANIFESTO-MESTRES.md` originalmente adicionados em `2026-08-27` (commit local `dd9ee76`), que nunca haviam sido enviados a este repositório remoto.
- **Motivo:** as fichas de personagem geradas em `2026-08-28` descreviam essas imagens como "ainda não versionadas em assets/" por não terem visibilidade sobre esse commit local; os arquivos e seus SHA-256 já existiam e não precisam ser reconstruídos.
- **Impacto:** os campos "Imagem MASTER: `A DEFINIR`" de `CHAR-001`, `CHAR-002`, `CHAR-004`, `CHAR-005`, `CHAR-006` e `CHAR-007` passam a apontar para os arquivos reais. `CHAR-003` (Patrícia) mantém uma ressalva específica: ver nota de reconciliação em `assets/personagens/mestres/MANIFESTO-MESTRES.md`.
- **Status:** `APROVADO`
- **Evidência:** [MANIFESTO-MESTRES.md](../assets/personagens/mestres/MANIFESTO-MESTRES.md)

## DEC-015

- **Data:** `2026-08-28`
- **Decisão:** migrar as MASTERs oficiais dos sete personagens (`CHAR-001` a `CHAR-007`) para a versão `V02 PHOTOREALISTIC`, fornecida pelo usuário como pacote `FAMILIA-SILVA-MASTERS-V02-PHOTOREALISTIC` (sete arquivos JPEG, `768x1376`, confirmados individualmente por correspondência visual a cada personagem antes da ingestão — ver [MANIFESTO-MESTRES.md](../assets/personagens/mestres/MANIFESTO-MESTRES.md)). A V02 passa a ser a referência visual `CURRENT CANON` para novas gerações de imagem e vídeo; a V01 é preservada como `HISTORICAL`, sem exclusão, e não deve ser escolhida automaticamente para novas cenas.
- **Motivo:** alinhar as referências visuais dos personagens ao padrão oficial `Photorealistic / Warm Cinematic Realism`, aumentando a consistência de geração image-to-video. Em testes recentes, a conversão de referências estilizadas (3D) para rendering fotorrealista mostrou-se instável — nem sempre reprodutível — mesmo com prompts corretos solicitando `Photorealistic / Warm Cinematic Realism`; usar uma referência de entrada já fotorrealista reduz esse conflito entre referência visual e estilo de rendering desejado. Ver aprendizado correspondente em [docs/APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md).
- **Impacto:** nenhuma identidade, persona, relação narrativa ou personalidade muda — a V02 é uma tradução fotorrealista/live-action do mesmo design de personagem aprovado, não um personagem diferente. Resolve a pendência histórica de longa data da MASTER V02 de Patrícia (`CHAR-003`), antes `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` em múltiplos documentos. Fichas de personagem, manifesto, changelog e template mestre atualizados para refletir a V02 como referência atual. Faixas etárias visuais aproximadas usadas como guia de casting/aparência na geração das V02 foram registradas nas fichas apenas como `visual age range`, não como idade narrativa canônica.
- **Status:** `APROVADO`
- **Evidência:** [MANIFESTO-MESTRES.md](../assets/personagens/mestres/MANIFESTO-MESTRES.md); pacote de origem `G:\Meu Drive\familia_silva\FAMILIA-SILVA-MASTERS-V02-PHOTOREALISTIC`

## DEC-016

- **Data:** `2026-08-29`
- **Decisão:** aprovar `ASSET-SERIES-001`, arquivo `IMG-FAMILIA-SILVA-PERFIL-V01.png`, como imagem institucional `V01` para os perfis oficiais da Família Silva no Instagram, Facebook, TikTok, YouTube e X.
- **Motivo:** estabelecer uma identidade visual única e reconhecível desde a criação dos perfis, reunindo o elenco fixo no rendering canônico `Photorealistic / Warm Cinematic Realism` e mantendo os sete rostos legíveis no recorte circular usado pelas plataformas.
- **Impacto:** o mesmo PNG quadrado deve ser usado em todas as redes, sem filtro, texto, logo, borda ou máscara circular pré-renderizada. A composição é um asset institucional; não substitui, altera ou promove qualquer rosto nela a nova imagem MASTER. As sete MASTERs V02 individuais permanecem as referências faciais primárias para novas gerações.
- **Status:** `APROVADO PARA USO EM PERFIS`
- **Evidência:** [registro de aprovação](../producao/aprovados/APROVACAO-IMAGEM-PERFIL-FAMILIA-SILVA-001.md); [manifesto do asset](../assets/logos/perfis/README.md); [prompt executado](../prompts/imagem/PROMPT-SERIES-IMAGE-001.md)

## DEC-017

- **Data:** `2026-08-29`
- **Decisão:** registrar `@familiasilvahumor` como o handle oficial e permanente do perfil da série Família Silva no TikTok, com status `CONFIGURADO`.
- **Motivo:** o perfil foi criado e configurado nesta data, confirmado diretamente pelo usuário; fixar o handle evita ambiguidade futura sobre qual conta é a oficial e cria uma fonte de verdade única para os canais da série ([REDES-SOCIAIS.md](REDES-SOCIAIS.md)).
- **Impacto:** o TikTok passa a constar como canal oficial já configurado em [REDES-SOCIAIS.md](REDES-SOCIAIS.md), [BIBLIA-DA-SERIE.md](BIBLIA-DA-SERIE.md) e [producao/STATUS.md](../producao/STATUS.md). A decisão limita-se ao handle e à existência do perfil: não define estratégia de conteúdo, frequência de postagem, monetização nem a adoção de outras plataformas, que permanecem `A DEFINIR`. Nenhum personagem, Character ID, MASTER, rendering, prompt, episódio, roteiro, regra de continuidade ou imagem institucional é alterado. A imagem de avatar dos perfis continua sendo `ASSET-SERIES-001` ([DEC-016](DECISOES.md#dec-016)).
- **Status:** `APROVADO`
- **Evidência:** confirmação direta do usuário em `2026-08-29`; [REDES-SOCIAIS.md](REDES-SOCIAIS.md); [CHANGELOG-CRIATIVO.md](CHANGELOG-CRIATIVO.md)

## DEC-018

- **Data:** `2026-08-29`
- **Decisão:** adotar como padrão preferencial condicional para novos vídeos da Família Silva a arquitetura de **vídeo contínuo multi-beat**, agrupando duas ou mais microcenas diretamente conectadas no mesmo vídeo quando a plataforma e a cena permitirem, em vez de dividir automaticamente cada microcena em um arquivo separado.
- **Motivo:** teste realizado no Gemini com vídeo de aproximadamente `20 segundos` reuniu duas microcenas consecutivas (Marcos pedindo a pasta a Patrícia e Dudu pedindo a camiseta a Patrícia) e apresentou, segundo avaliação direta do usuário, transição muito mais fluida. Um segundo teste reuniu a declaração da greve de Patrícia e a consequência imediata para Marcos procurando a chave reserva, também aprovado pelo usuário como resultado de alta qualidade.
- **Impacto:** o [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md) passa a orientar a avaliação de `beats` narrativos antes da segmentação em microclipes. A exclusividade de fala pode ser controlada por beat, sem revogar `LRN-011`; todos os locks e continuidades anteriores permanecem válidos. Microclipes continuam sendo fallback para cenas complexas, mudanças grandes de ambiente/tempo/figurino, alto risco de troca de fala/voz/lip sync, deriva em vídeo longo ou limitações da plataforma. A duração de `20 segundos` é evidência de capacidade observada no Gemini, não uma duração canônica universal e não deve virar instrução fixa no corpo do prompt.
- **Preservação:** esta decisão é um upgrade da pipeline e **não elimina nem substitui o conhecimento anterior**. As regras existentes de MASTER V02 própria, `Photorealistic / Warm Cinematic Realism`, prompt autossuficiente, simplificação controlada, continuidade visual, figurino, ambiente, relacionamento, fala, voz, lip sync e silêncio permanecem obrigatórias quando aplicáveis.
- **Status:** `APROVADO`
- **Evidência:** [LRN-015](APRENDIZADOS-DE-VIDEO.md#lrn-015--vídeo-contínuo-multi-beat-para-microcenas-encadeadas); [TESTE-VIDEO-MULTIBEAT-GEMINI-S01E001-001.md](../producao/testes/TESTE-VIDEO-MULTIBEAT-GEMINI-S01E001-001.md)

## Template de entrada

### DEC-XXX

- **Data:** `AAAA-MM-DD`
- **Decisão:** `A DEFINIR`
- **Motivo:** `A DEFINIR`
- **Impacto:** `A DEFINIR`
- **Status:** `A DEFINIR`
- **Evidência:** `A DEFINIR`
