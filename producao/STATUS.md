# Status de Produção

**Status geral:** FASE DE DESENVOLVIMENTO / PRÉ-PRODUÇÃO

## Áreas

- Bíblia e relações: `CONSOLIDADAS`.
- Personagens: sete IDs e sete personalidades canônicas.
- Rendering: `APROVADO` — `Photorealistic / Warm Cinematic Realism`.
- Template mestre de vídeo: `APROVADO` e definido como fonte única.
- Aprendizados: casos históricos, erros, soluções, aprovações e rejeições consolidados.
- Visual de Carol: `APROVADO VISUALMENTE`.
- Visual de Marcos, Dona Célia, Beto, Sr. Antônio e Dudu: `APROVADO / CANON VISUAL` (reconciliado pela [DEC-013](../docs/DECISOES.md#dec-013) em `2026-08-28`).
- Visual de Patrícia: `APROVADO / CANON VISUAL` — MASTER V02 PHOTOREALISTIC ingerida em `2026-08-28`, resolvendo a pendência histórica.
- Vozes: `A DEFINIR`.
- Assets MASTER no repositório: as sete imagens `V01` do elenco inicial foram versionadas e catalogadas pela [DEC-014](../docs/DECISOES.md#dec-014); as sete imagens `V02 PHOTOREALISTIC` foram versionadas e promovidas a `CURRENT CANON` pela [DEC-015](../docs/DECISOES.md#dec-015).
- Validação em vídeo das MASTERs V02: `CONCLUÍDA` para os 7 personagens em `2026-08-28` — um vídeo individual de apresentação por personagem no Google Flow, todos `APROVADO`/`APROVADA` pelo usuário (rendering `Photorealistic / Warm Cinematic Realism`, identidade visual consistente); ver `producao/testes/TESTE-VIDEO-*-002.md` (Dudu: `-001`).
- Auditoria física dos 7 vídeos de apresentação: `PARCIAL — BLOQUEADA POR ACESSO À FONTE BINÁRIA` em `2026-08-29`. A localização correta informada pelo usuário é `G:\Meu Drive\familia_silva\videos\apresentação da familia\`. Os arquivos históricos `marcos.mp4`, `celia.mp4`, `patricia.mp4`, `antonio.mp4`, `beto.mp4`, `carol.mp4` e `dudu.mp4` têm pareamento candidato documentado com os sete testes aprovados e nomenclatura alvo `VID-CHAR-XXX-APRESENTACAO-V01.mp4`, mas ainda não foram confirmados por inspeção do conteúdo nem renomeados fisicamente. Ver [AUDITORIA-VIDEOS-APRESENTACAO-2026-08-29.md](../docs/auditorias/AUDITORIA-VIDEOS-APRESENTACAO-2026-08-29.md).
- Imagem institucional de perfil: `APROVADA PARA USO EM PERFIS` em `2026-08-29` — `ASSET-SERIES-001`, arquivo quadrado `IMG-FAMILIA-SILVA-PERFIL-V01.png`, validado com os sete personagens e recorte circular seguro; ver [DEC-016](../docs/DECISOES.md#dec-016).
- Falas finais exatas das apresentações: o usuário alterou manualmente algumas falas antes da geração; o texto literal final não está disponível como fonte verificável — `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` para os 7 personagens.
- Falso positivo "pessoa famosa" no Flow: `PROCEDIMENTO DE FALLBACK VALIDADO` para Dudu, Sr. Antônio e Beto — ver [ERR-008](erros/ERR-008-FLOW-FALSO-POSITIVO-PESSOA-FAMOSA.md)/[SOL-008](solucoes/SOL-008-CONTEXTO-FICCIONAL-COMPLIANCE-FLOW.md); causa interna do classificador do Flow permanece desconhecida.
- Episódios: `S01E001` ("A Greve da Patrícia") `SOURCE_AVAILABLE — IMPORTED` em `2026-08-28` — roteiro completo, 12 cenas, 29 clipes, prompts originais e bíblia visual do episódio disponíveis; produção em vídeo clipe a clipe ainda não registrada (exceto Cena 2B, parcialmente documentada em `ERR-007`/`SOL-007`).
- Cenários: casa principal descrita em nível de episódio (S01E001), `PENDENTE DE PROMOÇÃO A CENÁRIO CANÔNICO REUTILIZÁVEL` em `cenarios/oficiais/`.
- Temporadas: `A DEFINIR`.
- Canal oficial (TikTok): `CONFIGURADO` em `2026-08-29` — perfil `@familiasilvahumor` (ver [REDES-SOCIAIS.md](../docs/REDES-SOCIAIS.md) e [DEC-017](../docs/DECISOES.md#dec-017)). Demais plataformas e a estratégia de distribuição permanecem `A DEFINIR`.

## Próximas ações necessárias

1. Produzir e aprovar uma referência neutra adicional de Dudu para uso futuro (sem gimbal/celular, boca fechada, tênis sem marca) — ver `ERR-006`/`SOL-006`; aplicável também à V02; não é bloqueante para uso da MASTER já aprovada.
2. Obter a versão revisada/aprovada exata do prompt da Cena 2B (S01E001) que efetivamente funcionou no Flow — hoje `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` (ver `SOL-007`).
3. Promover cozinha, sala e quarto de Marcos/Patrícia (bíblia visual de S01E001) a cenários canônicos reutilizáveis (`LOC-00X`) em `cenarios/oficiais/`, se decidido que valem para toda a série.
4. Gerar e registrar em `producao/testes/` os 29 clipes de S01E001, na ordem recomendada pela fonte histórica.
5. Aprovar e registrar a voz de cada personagem separadamente.
6. Definir cidade, época, duração padrão de episódio e público. Plataforma: o TikTok já está definido e configurado como canal oficial (`@familiasilvahumor`, `2026-08-29`); resta decidir se haverá distribuição em outras plataformas.
7. Avaliar o arquivo `G:\Meu Drive\familia_silva\patricia_silva.png` (fotorrealista, blusa terracota, fora do pacote V02) encontrado na auditoria de `2026-08-28` — não importado; ver nota em `MANIFESTO-MESTRES.md`.
8. Obter e importar o texto literal exato das falas finais dos 7 vídeos de apresentação (V02), alteradas manualmente pelo usuário antes da geração — hoje `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` em cada `producao/testes/TESTE-VIDEO-*-002.md` (Dudu: `-001`).
9. Desbloquear acesso aos sete `.mp4` da pasta `G:\Meu Drive\familia_silva\videos\apresentação da familia\` por Drive URL/ID ou upload direto; então inspecionar conteúdo e metadata, confirmar ou descartar os sete pareamentos candidatos, renomear fisicamente para `VID-CHAR-XXX-APRESENTACAO-V01.mp4`, registrar hashes e substituir `Asset de vídeo: A DEFINIR` nos sete registros de teste. Ver [auditoria de `2026-08-29`](../docs/auditorias/AUDITORIA-VIDEOS-APRESENTACAO-2026-08-29.md).

## Limite

Nenhum campo ausente deve ser inventado para encerrar uma pendência. Onde uma referência não foi versionada, ela permanece marcada como tal.
