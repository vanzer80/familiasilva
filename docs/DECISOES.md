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

## Template de entrada

### DEC-XXX

- **Data:** `AAAA-MM-DD`
- **Decisão:** `A DEFINIR`
- **Motivo:** `A DEFINIR`
- **Impacto:** `A DEFINIR`
- **Status:** `A DEFINIR`
- **Evidência:** `A DEFINIR`
