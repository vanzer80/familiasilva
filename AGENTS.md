# AGENTS

## Escopo

Este repositório é a fonte de verdade documental do projeto Família Silva. A organização e a rastreabilidade não autorizam a criação de conteúdo criativo. Toda informação ainda ausente deve permanecer como `A DEFINIR`.

## Fontes obrigatórias para vídeo

- A fonte executável para todo novo prompt de vídeo é [prompts/templates/TEMPLATE-MESTRE-VIDEO.md](prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- As decisões permanentes ficam em [docs/DECISOES.md](docs/DECISOES.md).
- Erros, acertos, hipóteses e soluções validadas ficam em [docs/APRENDIZADOS-DE-VIDEO.md](docs/APRENDIZADOS-DE-VIDEO.md) e nos registros de [producao/](producao/).
- Nenhum prompt pode depender de contexto, prompt ou vídeo anterior que a ferramenta de geração não recebeu. Cada prompt deve ser autossuficiente.

## Proteção de cânone

- Nunca alterar informação oficial de personagem sem autorização explícita.
- Nunca substituir silenciosamente uma decisão aprovada.
- Nunca promover um teste para material oficial automaticamente.
- Nunca tratar imagem experimental como imagem MASTER.
- Marcar materiais e decisões como `DEFINIDO`, `EM TESTE`, `APROVADO`, `APROVADO VISUALMENTE`, `APROVADO COM RESSALVAS`, `REJEITADO` ou `A DEFINIR`.
- Separar aprovação visual, vocal, narrativa e técnica. Aprovar uma dimensão não aprova automaticamente as demais.

## Personagens e versões

- Cada personagem possui um ID permanente, como `CHAR-001`.
- Cada personagem usa exclusivamente sua própria imagem MASTER ou referência visual aprovada.
- Um vídeo aprovado pode complementar o método de prompting ou rendering, mas não substitui a imagem MASTER como referência facial.
- Sr. Antônio (`CHAR-004`) e Beto (`CHAR-005`) são referências metodológicas para arquitetura de prompt e rendering, nunca referências faciais de outros personagens.
- Registrar mudanças visuais, de voz, de relação ou de continuidade no arquivo do personagem e no changelog criativo.
- Não apagar versões antigas relevantes. Preferir versionar arquivos ou registrar a alteração.

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

## Diálogo e voz

- Uma fala pertence exclusivamente ao personagem a que foi atribuída.
- Nunca trocar falas, aplicar a voz de um personagem a outro ou deixar um personagem completar a fala de outro.
- Personagens silenciosos não devem movimentar os lábios como se falassem.
- O lip sync deve pertencer apenas ao personagem que profere a fala correta.
- Voz ou fala experimental não se torna canônica por uma aprovação visual.

## Fluxo de materiais de IA

Todo resultado de IA entra primeiro em `producao/testes/`. Somente aprovação explícita permite classificá-lo como aprovado. Um material aprovado pode depois ser promovido a referência oficial ou MASTER com registro de decisão.

Para cada teste, registrar ferramenta, configuração, prompt ou sua situação de recuperação, referências, resultado, erros, correções, dimensão aprovada e impacto no cânone.

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

Se houver indicação de que o conteúdo já foi definido externamente, não reinventar: registrar o bloqueio (`PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` ou equivalente) e seguir apenas com o que está aprovado.
