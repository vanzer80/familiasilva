# Guia de Produção

## Fontes de verdade

- Cânone narrativo e visual: [BIBLIA-DA-SERIE.md](BIBLIA-DA-SERIE.md), [CONTINUIDADE.md](CONTINUIDADE.md) e fichas de personagens.
- Decisões permanentes: [DECISOES.md](DECISOES.md).
- Construção de prompts: [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- Erros, acertos e correções: [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md) e [producao/](../producao/).

## Princípios

- Usar este repositório como fonte oficial de verdade.
- Validar continuidade antes de gerar assets finais.
- Registrar prompts, imagens MASTER, vídeos, vozes e decisões relevantes.
- Marcar como `A DEFINIR` tudo que ainda não foi aprovado.
- Separar fato observado, hipótese de causa, solução testada e decisão canônica.
- Separar aprovação visual, vocal, narrativa e técnica.

## Antes de escrever um prompt de vídeo

1. Identificar personagem, Character ID, cena e status do material.
2. Consultar a ficha, personalidade e relações canônicas.
3. Confirmar qual referência visual pertence a cada personagem.
4. Usar somente imagem MASTER ou referência explicitamente aprovada do próprio personagem.
5. Consultar os erros e soluções já registrados.
6. Preencher o template mestre sem depender de contexto anterior.

## Ordem recomendada do prompt

1. `Fictional Context Declaration`.
2. Objetivo e personagens presentes.
3. Referências fornecidas nesta geração.
4. `Character Visual Continuity`.
5. `Series Rendering Style Continuity`.
6. `Costume Continuity` e `Environment Continuity`.
7. Cena, enquadramento, câmera, ação e atuação.
8. Diálogo literal e `Relationship Continuity`.
9. `Speaking Continuity`, `Voice Continuity`, `Lip-Sync Continuity` e `Silent Character Continuity`.
10. Áudio, restrições negativas e saída técnica.

Blocos sem aplicação real podem ser omitidos. Nenhum campo pode ser preenchido por invenção.

## Baseline validada para testes no Google Flow

- Caminho: `Vídeo → Elementos`, não Frames.
- Referências: anexadas como Elementos.
- Proporção: `9:16`.
- Modelo testado: `Veo 3.1 Lite`.
- Quantidade: `x1`.
- Duração de teste: `8s`.

Essa configuração é uma baseline de teste, não uma regra universal de episódio.

## Depois da geração

1. Registrar o resultado em [producao/testes/](../producao/testes/).
2. Aplicar [CHECKLIST-EPISODIO.md](../producao/CHECKLIST-EPISODIO.md) ou a parte relevante do checklist.
3. Registrar defeitos factuais em [producao/erros/](../producao/erros/).
4. Testar e registrar correções em [producao/solucoes/](../producao/solucoes/).
5. Guardar rejeições úteis em [producao/rejeitados/](../producao/rejeitados/).
6. Registrar aprovações explícitas em [producao/aprovados/](../producao/aprovados/).
7. Atualizar continuidade, ficha, changelog e decisões somente quando aplicável.

## Convenção de IDs

- Personagens: `CHAR-001`.
- Cenários: `LOC-001`.
- Episódios: `S01E001`.
- Assets: `ASSET-CHAR-001-001`.
- Prompts: `PROMPT-CHAR-001-VIDEO-001`.
- Testes: `TEST-VIDEO-CHAR-001-001`.
- Erros: `ERR-001`.
- Soluções: `SOL-001`.

## Regra de aprovação

Um item só passa a ser canônico quando:

1. Foi revisado.
2. Foi aprovado explicitamente na dimensão correta.
3. Foi registrado no documento adequado.
4. Recebeu ID quando aplicável.

Prompts e assets experimentais não definem cânone.
