# AI Onboarding — Família Silva

Este arquivo é o ponto de entrada recomendado para qualquer IA, agente ou colaborador que precise compreender, continuar, roteirizar ou produzir conteúdo do projeto **Família Silva**.

O repositório é a fonte oficial de verdade do projeto. Não use memória externa, suposições ou conhecimento geral para preencher lacunas de cânone.

## 1. Regra principal

**Não invente informação ausente.**

Um campo `A DEFINIR`, uma pasta vazia ou um item `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` não significa liberdade para criar uma resposta nova. Antes de concluir que algo não existe, verifique as fontes abaixo.

Se houver conflito entre documentos, preserve o histórico e aplique a decisão canônica mais recente e explicitamente aprovada. Em caso de dúvida real, sinalize a divergência em vez de escolher por conta própria.

## 2. Ordem mínima de leitura

Para compreender o projeto antes de executar qualquer tarefa relevante, leia nesta ordem:

1. [AGENTS.md](AGENTS.md) — regras operacionais, proteção de cânone e comportamento esperado de agentes.
2. [docs/BIBLIA-DA-SERIE.md](docs/BIBLIA-DA-SERIE.md) — identidade geral da série.
3. [docs/DECISOES.md](docs/DECISOES.md) — decisões permanentes, aprovações e supersessões.
4. [personagens/relacoes/RELACOES-FAMILIARES.md](personagens/relacoes/RELACOES-FAMILIARES.md) — relações canônicas.
5. [personagens/oficiais/](personagens/oficiais/) — fichas e personalidades canônicas dos personagens.
6. [docs/CONTINUIDADE.md](docs/CONTINUIDADE.md) — estado narrativo e continuidade entre materiais.
7. [docs/APRENDIZADOS-DE-VIDEO.md](docs/APRENDIZADOS-DE-VIDEO.md) — erros, acertos e regras aprendidas em produção.
8. [producao/STATUS.md](producao/STATUS.md) — estado atual, pendências e blockers.

Depois, leia as fontes específicas da tarefa.

## 3. Hierarquia prática de fontes

Use a seguinte precedência:

### Regras de agente e edição
- [AGENTS.md](AGENTS.md)

### Cânone geral e decisões
- [docs/BIBLIA-DA-SERIE.md](docs/BIBLIA-DA-SERIE.md)
- [docs/DECISOES.md](docs/DECISOES.md)
- [docs/CHANGELOG-CRIATIVO.md](docs/CHANGELOG-CRIATIVO.md) como histórico cronológico, não como substituto das decisões vigentes.

### Personagens
- ficha oficial em [personagens/oficiais/](personagens/oficiais/)
- personalidade canônica em [personagens/oficiais/personalidades/](personagens/oficiais/personalidades/)
- relações em [personagens/relacoes/RELACOES-FAMILIARES.md](personagens/relacoes/RELACOES-FAMILIARES.md)
- imagens MASTER e proveniência em [assets/personagens/mestres/MANIFESTO-MESTRES.md](assets/personagens/mestres/MANIFESTO-MESTRES.md)

### Continuidade narrativa
- [docs/CONTINUIDADE.md](docs/CONTINUIDADE.md)
- episódio correspondente em [episodios/](episodios/)

### Produção audiovisual
- [docs/APRENDIZADOS-DE-VIDEO.md](docs/APRENDIZADOS-DE-VIDEO.md)
- [producao/erros/](producao/erros/)
- [producao/solucoes/](producao/solucoes/)
- [producao/testes/](producao/testes/)
- [producao/aprovados/](producao/aprovados/)
- [producao/rejeitados/](producao/rejeitados/)

### Prompt de vídeo novo
A única fonte executável para a arquitetura de novos prompts é:

- [prompts/templates/TEMPLATE-MESTRE-VIDEO.md](prompts/templates/TEMPLATE-MESTRE-VIDEO.md)

Documentos históricos de episódios registram como determinado material foi criado na época, mas **não substituem o template mestre vigente**.

## 4. Se a tarefa for entender a Família Silva

Leia, no mínimo:

- [docs/BIBLIA-DA-SERIE.md](docs/BIBLIA-DA-SERIE.md)
- [docs/UNIVERSO.md](docs/UNIVERSO.md)
- [docs/TOM-E-HUMOR.md](docs/TOM-E-HUMOR.md)
- [personagens/README.md](personagens/README.md)
- [personagens/relacoes/RELACOES-FAMILIARES.md](personagens/relacoes/RELACOES-FAMILIARES.md)
- as fichas e personalidades dos personagens relevantes
- [docs/DECISOES.md](docs/DECISOES.md)
- [producao/STATUS.md](producao/STATUS.md)

## 5. Se a tarefa for criar roteiro, cena ou diálogo

Antes de escrever:

1. leia a ficha e a personalidade de todos os personagens da cena;
2. leia as relações entre eles;
3. leia [docs/TOM-E-HUMOR.md](docs/TOM-E-HUMOR.md);
4. leia [docs/CONTINUIDADE.md](docs/CONTINUIDADE.md);
5. leia os episódios anteriores relevantes;
6. verifique [docs/DECISOES.md](docs/DECISOES.md) para regras narrativas vigentes.

Não copie diálogos, bordões, cenas, aparência, figurino ou caracterizações de obras de referência. Referências externas como *A Grande Família* são metodológicas e estruturais, nunca autorização para reprodução literal.

## 6. Se a tarefa for gerar um vídeo

Antes de produzir o prompt, leia obrigatoriamente:

1. [prompts/templates/TEMPLATE-MESTRE-VIDEO.md](prompts/templates/TEMPLATE-MESTRE-VIDEO.md);
2. ficha oficial e personalidade de cada personagem presente;
3. [personagens/relacoes/RELACOES-FAMILIARES.md](personagens/relacoes/RELACOES-FAMILIARES.md);
4. [assets/personagens/mestres/MANIFESTO-MESTRES.md](assets/personagens/mestres/MANIFESTO-MESTRES.md);
5. [docs/APRENDIZADOS-DE-VIDEO.md](docs/APRENDIZADOS-DE-VIDEO.md);
6. erros e soluções relevantes em `producao/`;
7. episódio/cena correspondente, se existir;
8. [docs/CONTINUIDADE.md](docs/CONTINUIDADE.md).

### Regras essenciais de vídeo

- Rendering canônico: `Photorealistic / Warm Cinematic Realism`.
- Cada personagem usa sua própria MASTER ou referência aprovada.
- Não usar a aparência de um personagem como referência facial de outro.
- Cada prompt deve ser autossuficiente.
- Aplicar continuidades de personagem, rendering, figurino, ambiente, relação, fala, voz, lip sync e silêncio quando forem pertinentes.
- Quando houver risco de troca de fala, priorizar um falante principal e manter os demais explicitamente silenciosos.
- Mais restrições não significam automaticamente melhor resultado; usar apenas as restrições necessárias para a cena.
- Por padrão, não inserir duração fixa em segundos no texto operacional do prompt. Duração editorial/configuração de ferramenta é separada do conteúdo textual enviado ao gerador.
- Não colocar IDs, nomes internos de clipes, cabeçalhos administrativos ou metadados desnecessários dentro do prompt final se houver risco de aparecerem no vídeo.

## 7. Episódio 1 como referência de produção

O Episódio 1, **S01E001 — A Greve da Patrícia**, está importado no repositório.

Use:

- [episodios/S01/S01E001-A-GREVE-DA-PATRICIA.md](episodios/S01/S01E001-A-GREVE-DA-PATRICIA.md) — índice e estado consolidado.
- [episodios/S01/FONTE-HISTORICA-S01E001-A-GREVE-DA-PATRICIA.md](episodios/S01/FONTE-HISTORICA-S01E001-A-GREVE-DA-PATRICIA.md) — fonte histórica de produção.

A fonte histórica preserva instruções e prompts usados na época. Ela pode conter práticas posteriormente substituídas. Para criar material novo, sempre prevalecem o template mestre e os aprendizados atuais.

## 8. Cena 2B — cuidado especial

O repositório possui o roteiro canônico e o prompt original da Cena 2B, além dos aprendizados derivados do caso.

Consulte:

- `producao/erros/ERR-007-CENA-2B-TENTATIVA-INICIAL.md`
- `producao/solucoes/SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md`

A versão revisada/aprovada exata do prompt que efetivamente funcionou no Flow ainda pode estar marcada como `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA`. Não reconstruir essa versão por suposição e não substituir automaticamente a fala canônica do roteiro por uma variante de produção.

## 9. Materiais históricos versus regra atual

Nunca "corrija" um documento histórico para fazê-lo parecer compatível com uma regra posterior.

Exemplo: prompts históricos podem mencionar duração aproximada de 8 segundos. Isso registra como o episódio foi planejado naquela fase. A regra operacional atual para novos prompts é definida pelo template mestre e pelos aprendizados vigentes.

Preserve sempre a distinção entre:

- roteiro canônico;
- prompt histórico;
- variante de teste;
- solução aprovada;
- aprendizado reutilizável;
- regra operacional atual.

## 10. Status e lacunas

Para saber o que está realmente pronto ou pendente, consulte sempre:

- [producao/STATUS.md](producao/STATUS.md)

Não use snapshots antigos de status em outros documentos como fonte superior ao STATUS atual e às decisões formais.

Itens ainda não definidos ou ainda não importados não devem bloquear tarefas que não dependem deles. Por exemplo, um cenário ainda não promovido a `LOC-00X` não impede necessariamente a criação de uma cena quando a ambientação necessária já está sustentada por um episódio ou por outra fonte aprovada.

## 11. Antes de entregar qualquer resultado

Cheque:

- Estou usando os personagens corretos e seus IDs corretos?
- Li as personalidades e relações relevantes?
- Estou respeitando decisões mais recentes?
- Estou confundindo material histórico com regra atual?
- Estou inventando algo marcado `A DEFINIR` ou `PENDENTE DE IMPORTAÇÃO`?
- Para vídeo, usei o template mestre vigente?
- Consultei aprendizados, erros e soluções relevantes?
- Minha saída contradiz continuidade já registrada?

Se qualquer resposta for incerta, reporte a incerteza em vez de criar cânone por conta própria.

## 12. Objetivo deste repositório

Uma IA nova deve conseguir, somente a partir deste repositório:

- compreender o universo e a proposta da Família Silva;
- entender quem é cada personagem e como se relacionam;
- distinguir cânone, teste, histórico e pendência;
- escrever cenas coerentes com personalidade e continuidade;
- gerar prompts de vídeo de acordo com as regras de produção atuais;
- reutilizar erros e soluções já aprendidos sem repetir falhas conhecidas;
- continuar o projeto sem depender de conversas antigas, salvo nos pontos explicitamente marcados como pendentes de importação.
