# Família Silva

**Status:** FASE DE DESENVOLVIMENTO / PRÉ-PRODUÇÃO

Família Silva é uma sitcom familiar brasileira original, produzida com apoio de Inteligência Artificial e planejada para crescer sem perder continuidade narrativa, visual e sonora.

Este repositório é a **fonte oficial de verdade** do projeto.

## Para IAs, GPTs, Skills e agentes

Se você é uma IA, agente, GPT personalizado, Skill, Claude Code, Gemini, Codex ou outro sistema que precisa compreender ou continuar o projeto, **comece obrigatoriamente por:**

- [AI-ONBOARDING.md](AI-ONBOARDING.md) — ordem de leitura, hierarquia de autoridade, regras de precedência, modos de tarefa e teste de onboarding.
- [AGENTS.md](AGENTS.md) — regras operacionais e proteção de cânone.

Não presuma que ausência de informação autoriza invenção.

## Comece por aqui

- [AI Onboarding](AI-ONBOARDING.md) — ponto de entrada oficial para IAs e agentes.
- [Bíblia da Série](docs/BIBLIA-DA-SERIE.md) — universo e cânone geral.
- [Decisões](docs/DECISOES.md) — decisões permanentes, reconciliações e supersessões.
- [Continuidade](docs/CONTINUIDADE.md) — estado narrativo e eventos anteriores.
- [Aprendizados de Vídeo](docs/APRENDIZADOS-DE-VIDEO.md) — erros, acertos, hipóteses e correções consolidadas.
- [Template Mestre de Vídeo](prompts/templates/TEMPLATE-MESTRE-VIDEO.md) — única fonte executável para novos prompts de vídeo.
- [Guia de Produção](docs/GUIA-DE-PRODUCAO.md) — fluxo de trabalho.
- [Status de Produção](producao/STATUS.md) — estado operacional atual, pendências e blockers.
- [Redes Sociais Oficiais](docs/REDES-SOCIAIS.md) — perfis e canais oficiais já configurados e os que faltam.

## Decisões audiovisuais vigentes

- Rendering canônico: `Photorealistic / Warm Cinematic Realism`.
- Cada prompt deve ser autossuficiente.
- Cada personagem usa exclusivamente sua própria imagem MASTER ou referência aprovada.
- Sr. Antônio e Beto são referências metodológicas de prompt e rendering, nunca referências faciais de outros personagens.
- Fala, voz, lip sync e silêncio são continuidades separadas e explicitamente vinculadas.
- Aprovação visual não aprova automaticamente voz, diálogo, atuação ou dinâmica narrativa.
- Para novos prompts de vídeo, prevalecem o template mestre e os aprendizados atuais; documentos históricos preservam o método usado na época e não substituem regras vigentes.

## Filosofia

- Consistência visual e narrativa em todos os materiais.
- Continuidade clara entre episódios, temporadas, personagens e cenários.
- Produção assistida por IA com revisão humana e registro de evidências.
- Hipóteses separadas de fatos e decisões.
- Proteção de propriedade intelectual própria: referências externas podem orientar arquétipos, funções narrativas e mecanismos gerais, mas não autorizam cópia de personagens, histórias, nomes, cenários, diálogos, bordões, aparência, figurino ou trejeitos.
- O repositório deve concentrar conhecimento; agentes externos devem funcionar como camada de comportamento sobre essa fonte, não como uma segunda Bíblia do projeto.

## Regra de cânone

Somente informações aprovadas e registradas nos documentos oficiais são cânone.

- `A DEFINIR` = ainda não existe decisão suficiente.
- `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` = a informação já existe fora do repositório, mas a fonte ainda não foi versionada; **não reconstruir por suposição**.
- material histórico permanece histórico mesmo quando uma regra posterior o substitui operacionalmente.

Para conflitos e precedência entre decisões, consulte [docs/DECISOES.md](docs/DECISOES.md); não use apenas número ou data como critério.

## Estrutura

- [docs/](docs/) — bíblia, universo, tom, continuidade, decisões, guia e aprendizados.
- [personagens/](personagens/) — cadastro, fichas, personalidades, relações e regras.
- [cenarios/](cenarios/) — índice e templates de cenários.
- [episodios/](episodios/) — episódios, índices e fontes históricas de produção.
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

## Elenco inicial

| ID | Nome canônico | Estado resumido |
|---|---|---|
| `CHAR-001` | Marcos Silva | `APROVADO / CANON VISUAL` |
| `CHAR-002` | Dona Célia | `APROVADO / CANON VISUAL` |
| `CHAR-003` | Patrícia Silva | `APROVADO / CANON VISUAL` — MASTER V02 PHOTOREALISTIC (current canon) |
| `CHAR-004` | Sr. Antônio | `APROVADO / CANON VISUAL`; vizinho recorrente, não membro oficial da Família Silva |
| `CHAR-005` | Beto | `APROVADO / CANON VISUAL` |
| `CHAR-006` | Carol Silva | `APROVADO VISUALMENTE` |
| `CHAR-007` | Dudu Silva | `APROVADO / CANON VISUAL` |

Os sete personagens possuem Character IDs permanentes, relações consolidadas e personalidades canônicas em `personagens/oficiais/`.

## Estado atual

O repositório está reconciliado e concentra hoje a maior parte do conhecimento já produzido do projeto:

- sete Character IDs permanentes;
- sete personalidades canônicas;
- relações familiares consolidadas;
- sete imagens MASTER `V02 PHOTOREALISTIC` versionadas e catalogadas como `CURRENT CANON`; V01 preservada como `HISTORICAL`;
- rendering canônico definido;
- arquitetura mestre de prompts de vídeo aprovada;
- base de erros, soluções, testes e aprendizados populada;
- `S01E001 — A Greve da Patrícia` importado, com roteiro completo, 12 cenas, 29 clipes, prompts originais e bíblia visual histórica;
- Cena 2B documentada com roteiro e prompt original, mantendo pendente apenas a versão revisada/aprovada exata e detalhes não recuperados;
- cozinha, sala e quarto do casal descritos no Episódio 1, ainda não necessariamente promovidos a cenários canônicos reutilizáveis;
- vozes ainda `A DEFINIR` até aprovação específica.

Para o estado operacional mais atualizado e a lista completa de pendências, **não use esta seção como substituto do status vivo**. Consulte sempre:

- [producao/STATUS.md](producao/STATUS.md)

## Princípio final

Uma nova IA deve conseguir entrar neste repositório, seguir [AI-ONBOARDING.md](AI-ONBOARDING.md), localizar as fontes corretas e trabalhar sem depender de conversas antigas — exceto nos pontos explicitamente marcados como pendentes de importação ou ainda não definidos.
