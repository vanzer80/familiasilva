# Prompts

Este diretório organiza os prompts usados na produção de Família Silva.

## Fonte oficial

[templates/TEMPLATE-MESTRE-VIDEO.md](templates/TEMPLATE-MESTRE-VIDEO.md) é a única fonte executável para a arquitetura de novos prompts de vídeo.

- Não criar um segundo template mestre concorrente.
- Não depender de prompt ou vídeo anterior não fornecido à ferramenta.
- Consultar [../docs/APRENDIZADOS-DE-VIDEO.md](../docs/APRENDIZADOS-DE-VIDEO.md) antes de gerar um novo vídeo.
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
