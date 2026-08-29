# Prompts

Este diretório organiza os prompts usados na produção de Família Silva.

## Fonte oficial

[templates/TEMPLATE-MESTRE-VIDEO.md](templates/TEMPLATE-MESTRE-VIDEO.md) é a única fonte executável para a arquitetura de novos prompts de vídeo.

- Não criar um segundo template mestre concorrente.
- Não depender de prompt ou vídeo anterior não fornecido à ferramenta.
- Consultar [../docs/APRENDIZADOS-DE-VIDEO.md](../docs/APRENDIZADOS-DE-VIDEO.md) e o adendo validado de S01E001 em [../docs/APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md](../docs/APRENDIZADOS-S01E001-VALIDACAO-FINAL-2026-08-29.md) antes de gerar um novo vídeo.
- Antes de entregar qualquer prompt, passar pela checklist e comparar com os Reference Examples (ilustrativos, não verificados em produção) e os erros conhecidos no fim de [templates/TEMPLATE-MESTRE-VIDEO.md](templates/TEMPLATE-MESTRE-VIDEO.md).
- Antes de segmentar automaticamente um roteiro em microclipes, avaliar se microcenas diretamente conectadas podem ser agrupadas como beats em um único vídeo contínuo. O benefício validado é narrativo: transições e causalidade podem ficar mais fluidas. **Não assumir uma duração específica nem que `20s` sejam sempre uma geração única direta; validar a operação real da ferramenta.**
- O formato multi-beat não remove os conhecimentos anteriores: cada beat continua sujeito a referências MASTER próprias, rendering canônico, continuidade, atribuição de fala, voz, lip sync e silêncio. Quando o vídeo longo aumentar o risco de erro, voltar a microclipes.
- **Gemini, múltiplas referências:** anexar todas as MASTERs citadas no prompt e, na rodada validada de `2026-08-29`, manter a mesma ordem entre os nomes na frase de referência e os arquivos anexados. Ver [ERR-009](../producao/erros/ERR-009-GEMINI-MASTERS-AUSENTES-OU-FORA-DE-ORDEM.md) / [SOL-009](../producao/solucoes/SOL-009-GEMINI-MASTERS-COMPLETAS-E-ORDENADAS.md).
- Escrever falas para **interpretação oral real**, não apenas para caber em uma contagem de caracteres. Emoção, pausa e reação consomem tempo; se a fala ficar apertada, reduzir palavras antes de sacrificar naturalidade.
- Preferir diálogo coloquial e emocionalmente específico: interjeições, pequenas repetições, hesitações e pausas naturais são válidas quando coerentes com a personalidade.
- Usar somente informações aprovadas; campos ausentes permanecem `A DEFINIR`.
- Prompts não aprovados são materiais de trabalho, não cânone.

## Subdiretórios

- [imagem/](imagem/) — prompts de imagens, personagens, cenários e referências visuais.
- [video/](video/) — instruções específicas das ferramentas audiovisuais.
- [voz/](voz/) — prompts e direções de voz, fala e interpretação.
- [templates/](templates/) — modelos reutilizáveis.
- [mestres/](mestres/) — instâncias de prompts promovidas explicitamente a mestre; não usar como depósito de testes.

## Convenção de IDs

Use `PROMPT-CHAR-001-VIDEO-001`, adaptando o tipo:

- `IMAGE`.
- `VIDEO`.
- `VOICE`.

Todo prompt deve indicar personagem, cenário, episódio ou asset relacionado, além da versão e do status.

## Rendering obrigatório

O padrão aprovado é `Photorealistic / Warm Cinematic Realism`. O estilo deve ser descrito tecnicamente, sem nomes de estúdios, franquias, obras ou artistas.
