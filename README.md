# Família Silva

**Status:** FASE DE DESENVOLVIMENTO / PRÉ-PRODUÇÃO

Família Silva é uma sitcom familiar brasileira original, produzida com apoio de Inteligência Artificial e planejada para crescer sem perder continuidade narrativa, visual e sonora.

Este repositório é a fonte oficial de verdade do projeto.

## Comece por aqui

- [Bíblia da Série](docs/BIBLIA-DA-SERIE.md) — universo e cânone geral.
- [Decisões](docs/DECISOES.md) — decisões permanentes aprovadas.
- [Continuidade](docs/CONTINUIDADE.md) — estado dos personagens e elementos recorrentes.
- [Aprendizados de Vídeo](docs/APRENDIZADOS-DE-VIDEO.md) — erros, acertos, hipóteses e correções consolidadas.
- [Template Mestre de Vídeo](prompts/templates/TEMPLATE-MESTRE-VIDEO.md) — única fonte executável para novos prompts.
- [Guia de Produção](docs/GUIA-DE-PRODUCAO.md) — fluxo de trabalho.
- [Status de Produção](producao/STATUS.md) — pendências atuais.

## Decisões audiovisuais vigentes

- Rendering canônico: `Photorealistic / Warm Cinematic Realism`.
- Cada prompt deve ser autossuficiente.
- Cada personagem usa exclusivamente sua própria imagem MASTER ou referência aprovada.
- Sr. Antônio e Beto são referências metodológicas de prompt e rendering, nunca referências faciais de outros personagens.
- Fala, voz, lip sync e silêncio são continuidades separadas e explicitamente vinculadas.
- Aprovação visual não aprova automaticamente voz, diálogo, atuação ou dinâmica narrativa.

## Filosofia

- Consistência visual e narrativa em todos os materiais.
- Continuidade clara entre episódios, temporadas, personagens e cenários.
- Produção assistida por IA com revisão humana e registro de evidências.
- Hipóteses separadas de fatos e decisões.
- Proteção de propriedade intelectual própria: a série pode se inspirar em dinâmicas gerais de sitcom familiar brasileira, mas não copia personagens, histórias, nomes, cenários, diálogos, bordões, aparência, figurino ou trejeitos de outras obras.

## Regra de cânone

Somente informações aprovadas e registradas nos documentos oficiais são cânone. Informações marcadas como `A DEFINIR`, hipótese, conceito, rascunho ou em desenvolvimento não são cânone.

## Estrutura

- [docs/](docs/) — bíblia, universo, tom, continuidade, decisões, guia e aprendizados.
- [personagens/](personagens/) — cadastro, fichas, personalidades, relações e regras.
- [cenarios/](cenarios/) — índice e templates de cenários.
- [episodios/](episodios/) — índice e templates de episódios.
- [temporadas/](temporadas/) — organização de temporadas.
- [prompts/](prompts/) — prompts de imagem, vídeo, voz e templates.
- [assets/](assets/) — imagens MASTER, referências, logos e áudio.
- [producao/](producao/) — workflow, checklist, testes, erros, soluções, aprovações e status.
- [tools/](tools/) — ferramentas auxiliares.

## Convenção de IDs

- Personagens: `CHAR-001`.
- Cenários: `LOC-001`.
- Episódios: `S01E001`.
- Assets: `ASSET-CHAR-001-001`.
- Prompts: `PROMPT-CHAR-001-VIDEO-001`.
- Testes: `TEST-VIDEO-CHAR-001-001`.
- Erros: `ERR-001`.
- Soluções: `SOL-001`.

## Estado atual

O elenco inicial possui sete IDs permanentes e sete personalidades canônicas. O rendering da série e a arquitetura de prompts de vídeo estão aprovados. Carol possui teste aprovado visualmente; Marcos, Dona Célia, Patrícia, Sr. Antônio e Beto têm referências visuais aprovadas com ressalvas; Dudu precisa de uma nova referência neutra. Os arquivos visuais informados ainda precisam ser versionados em `assets/`, e as vozes permanecem `A DEFINIR` até aprovação específica.
