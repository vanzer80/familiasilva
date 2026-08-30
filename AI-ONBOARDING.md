# AI Onboarding V2 — Família Silva

> **Ponto de entrada oficial para IAs, agentes, GPTs personalizados, Skills, Claude Code, Gemini, Codex e colaboradores humanos.**

Este repositório é a **fonte oficial de verdade documental** do projeto **Família Silva**.

O objetivo deste arquivo não é duplicar a Bíblia, as fichas, as decisões ou os aprendizados. Sua função é explicar **o que ler, em que ordem, qual fonte prevalece, como executar cada tipo de tarefa e como evitar reinventar cânone já definido**.

---

## 1. Regra máxima

**Não invente informação ausente.**

Um campo `A DEFINIR`, uma pasta vazia ou um item `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` não significa liberdade para criar novo cânone.

Antes de concluir que algo não existe:

1. procure nas fontes canônicas indicadas neste onboarding;
2. verifique decisões e continuidade;
3. verifique se a informação está marcada como pendente de importação;
4. somente depois classifique como realmente indefinida.

Se houver incerteza real, **sinalize a incerteza**. Não resolva conflito de cânone por adivinhação.

---

## 2. Missão do repositório

Uma IA nova deve conseguir, somente a partir deste repositório:

- compreender a proposta e o universo da Família Silva;
- identificar os personagens e suas relações;
- compreender personalidade, função narrativa, tom de fala e limites de comportamento;
- distinguir cânone, histórico, teste, hipótese, erro, solução, aprovação e pendência;
- escrever cenas e diálogos coerentes;
- gerar prompts de vídeo conforme as regras atuais;
- reutilizar aprendizados de produção;
- evitar repetir erros já conhecidos;
- continuar episódios e continuidade narrativa;
- criar uma camada externa de agente/GPT/Skill sem transformar essa camada em uma segunda fonte de verdade.

---

## 3. Ordem mínima obrigatória de leitura

Antes de executar qualquer tarefa relevante, leia nesta ordem:

1. [AI-ONBOARDING.md](AI-ONBOARDING.md) — este arquivo.
2. [AGENTS.md](AGENTS.md) — regras operacionais e proteção de cânone.
3. [docs/BIBLIA-DA-SERIE.md](docs/BIBLIA-DA-SERIE.md) — identidade geral da série.
4. [docs/DECISOES.md](docs/DECISOES.md) — decisões formais, aprovações e supersessões.
5. [personagens/relacoes/RELACOES-FAMILIARES.md](personagens/relacoes/RELACOES-FAMILIARES.md) — relações canônicas.
6. fichas e personalidades dos personagens relevantes em [personagens/oficiais/](personagens/oficiais/).
7. [docs/CONTINUIDADE.md](docs/CONTINUIDADE.md) — continuidade narrativa e eventos anteriores.
8. [docs/APRENDIZADOS-DE-VIDEO.md](docs/APRENDIZADOS-DE-VIDEO.md) — conhecimento consolidado de produção audiovisual.
9. [docs/APRENDIZADOS-EM-VALIDACAO.md](docs/APRENDIZADOS-EM-VALIDACAO.md) — hipóteses e observações de produção ainda `EM TESTE`, antes de virarem regra oficial.
10. [producao/STATUS.md](producao/STATUS.md) — estado atual, blockers e pendências.

Depois disso, leia as fontes específicas da tarefa.

---

## 4. Hierarquia real de autoridade

### 4.1 Regras de agente e edição

1. [AGENTS.md](AGENTS.md)
2. este `AI-ONBOARDING.md` como guia de navegação e execução

### 4.2 Decisões e cânone geral

1. [docs/DECISOES.md](docs/DECISOES.md)
2. [docs/BIBLIA-DA-SERIE.md](docs/BIBLIA-DA-SERIE.md)
3. documentos especializados da área afetada

[docs/CHANGELOG-CRIATIVO.md](docs/CHANGELOG-CRIATIVO.md) é **histórico cronológico**. Ele não substitui uma decisão formal vigente.

### 4.3 Estado atual

Para status operacional e pendências, consulte:

- [producao/STATUS.md](producao/STATUS.md)

Snapshots antigos de status em outros documentos não prevalecem sobre `STATUS.md` e decisões formais.

### 4.4 Regra de precedência entre decisões

**Não use apenas o número da DEC ou a data para decidir o que prevalece.**

O repositório possui decisões reconciliadas de linhas históricas diferentes. Leia:

- a seção de reconciliação de [docs/DECISOES.md](docs/DECISOES.md);
- especialmente `DEC-013`, que formaliza precedência em conflitos de aprovação visual baseados em evidência de produção real.

Uma decisão marcada como `SUPERADO`, `HISTÓRICO` ou explicitamente substituída **não é regra operacional vigente**.

### 4.5 Quando ainda houver conflito

Se duas fontes oficiais parecerem incompatíveis e `docs/DECISOES.md` não resolver a precedência:

- não escolha sozinho;
- preserve ambas;
- reporte `CONFLITO DE CÂNONE / REQUER DECISÃO HUMANA`.

---

## 5. Mapa canônico dos personagens

Os Character IDs permanentes são:

| ID | Nome canônico | Papel relacional básico |
|---|---|---|
| `CHAR-001` | Marcos Silva | marido de Patrícia; pai de Carol e Dudu; filho de Dona Célia |
| `CHAR-002` | Dona Célia | mãe de Marcos; avó de Carol e Dudu |
| `CHAR-003` | Patrícia Silva | esposa de Marcos; mãe de Carol e Dudu |
| `CHAR-004` | Sr. Antônio | vizinho recorrente; **não integrante oficial da Família Silva** |
| `CHAR-005` | Beto | marido de Carol; genro de Marcos e Patrícia |
| `CHAR-006` | Carol Silva | filha de Marcos e Patrícia; irmã de Dudu; esposa de Beto |
| `CHAR-007` | Dudu Silva | filho de Marcos e Patrícia; irmão de Carol |

A tabela acima é apenas um **mapa de navegação**. Para detalhes e nuances, prevalecem as fichas e a matriz oficial de relações.

### Personalidades canônicas — arquivos exatos

- [MARCOS-PERSONALIDADE.md](personagens/oficiais/personalidades/MARCOS-PERSONALIDADE.md)
- [PATRICIA-PERSONALIDADE.md](personagens/oficiais/personalidades/PATRICIA-PERSONALIDADE.md)
- [CAROL-PERSONALIDADE.md](personagens/oficiais/personalidades/CAROL-PERSONALIDADE.md)
- [DUDU-PERSONALIDADE.md](personagens/oficiais/personalidades/DUDU-PERSONALIDADE.md)
- [BETO-PERSONALIDADE.md](personagens/oficiais/personalidades/BETO-PERSONALIDADE.md)
- [DONA-CELIA-PERSONALIDADE.md](personagens/oficiais/personalidades/DONA-CELIA-PERSONALIDADE.md)
- [ANTONIO-PERSONALIDADE.md](personagens/oficiais/personalidades/ANTONIO-PERSONALIDADE.md)

Nunca deduza personalidade apenas de aparência, vídeo, nome, arquétipo ou relação familiar.

---

## 6. Modo: entender o projeto

Se a tarefa for explicar ou compreender a Família Silva, leia no mínimo:

- [docs/BIBLIA-DA-SERIE.md](docs/BIBLIA-DA-SERIE.md)
- [docs/UNIVERSO.md](docs/UNIVERSO.md)
- [docs/TOM-E-HUMOR.md](docs/TOM-E-HUMOR.md)
- [personagens/README.md](personagens/README.md)
- [personagens/relacoes/RELACOES-FAMILIARES.md](personagens/relacoes/RELACOES-FAMILIARES.md)
- as sete personalidades, ou pelo menos as dos personagens envolvidos na pergunta
- [docs/DECISOES.md](docs/DECISOES.md)
- [docs/CONTINUIDADE.md](docs/CONTINUIDADE.md)
- [producao/STATUS.md](producao/STATUS.md)

Ao responder, diferencie claramente:

- fato canônico;
- histórico;
- pendência;
- hipótese;
- interpretação.

---

## 7. Modo: criar roteiro, cena ou diálogo

Antes de escrever:

1. leia a ficha oficial de cada personagem da cena;
2. leia a personalidade de cada personagem da cena;
3. leia as relações entre eles;
4. leia [docs/TOM-E-HUMOR.md](docs/TOM-E-HUMOR.md);
5. leia [docs/CONTINUIDADE.md](docs/CONTINUIDADE.md);
6. leia os episódios anteriores relevantes;
7. verifique [docs/DECISOES.md](docs/DECISOES.md);
8. verifique se existe restrição ou aprendizado de produção que afete a cena.

### Referências externas

*A Grande Família* é referência metodológica de arquétipos, funções narrativas, dinâmica doméstica e mecanismos de humor.

Não copiar:

- personagens;
- diálogos;
- bordões;
- cenas;
- histórias específicas;
- aparência;
- figurino;
- cenários reconhecíveis;
- trejeitos exclusivos.

Família Silva deve permanecer uma obra original.

---

## 8. Modo: gerar vídeo ou prompt de vídeo

A única fonte executável para a arquitetura de **novos prompts de vídeo** é:

- [prompts/templates/TEMPLATE-MESTRE-VIDEO.md](prompts/templates/TEMPLATE-MESTRE-VIDEO.md)

Antes de gerar qualquer prompt, leia obrigatoriamente:

1. o template mestre;
2. ficha e personalidade de cada personagem presente;
3. [personagens/relacoes/RELACOES-FAMILIARES.md](personagens/relacoes/RELACOES-FAMILIARES.md);
4. [assets/personagens/mestres/MANIFESTO-MESTRES.md](assets/personagens/mestres/MANIFESTO-MESTRES.md);
5. [docs/APRENDIZADOS-DE-VIDEO.md](docs/APRENDIZADOS-DE-VIDEO.md);
6. [docs/APRENDIZADOS-EM-VALIDACAO.md](docs/APRENDIZADOS-EM-VALIDACAO.md) — para saber quais hipóteses estão `EM TESTE` nesta fase e não tratá-las como regra fechada;
7. erros, soluções e testes relevantes em `producao/`;
8. episódio/cena correspondente, quando existir;
9. [docs/CONTINUIDADE.md](docs/CONTINUIDADE.md).

### Regras essenciais de vídeo

- Rendering canônico: `Photorealistic / Warm Cinematic Realism`.
- Cada personagem usa exclusivamente sua própria MASTER ou referência aprovada.
- Nunca usar o rosto de outro personagem como referência facial.
- Sr. Antônio e Beto podem servir como referências **metodológicas** de prompting/rendering, nunca como referência facial para outros.
- Cada prompt deve ser autossuficiente.
- Aplicar, quando pertinentes, continuidades de personagem, rendering, figurino, ambiente, relação, fala, voz, lip sync e silêncio.
- Quando houver risco de troca de fala, priorizar um falante principal e manter os demais explicitamente silenciosos.
- Mais negative constraints não significam automaticamente melhor geração; usar apenas restrições necessárias e úteis.
- Por padrão, não inserir duração fixa em segundos no texto operacional do prompt. Duração editorial/configuração de ferramenta é separada do conteúdo textual enviado ao gerador.
- Evitar IDs, nomes internos de clipes, títulos administrativos, cabeçalhos técnicos e metadados desnecessários dentro do prompt final quando houver risco de aparecerem no vídeo.
- Não usar `CHARACTER IDENTITY LOCK` ou `EXACTLY the same person` como instruções operacionais ativas.
- Ao continuar uma sequência já em produção, antes de escrever a próxima cena verifique o **último material audiovisual aprovado disponível** e reconcilie-o com o roteiro planejado; em conflito factual, a continuidade realizada prevalece para o ponto de partida, e o roteiro segue orientando o arco futuro (hipótese [AV-008](docs/APRENDIZADOS-EM-VALIDACAO.md#av-008--continuidade-realizada-tem-precedência-operacional-sobre-roteiro-planejado), ainda `EM TESTE` — não é regra fechada).

Antes de entregar qualquer prompt, use a checklist, os "Reference Examples — illustrative, not production-verified" e a seção "Erros conhecidos e como evitar regressões" ao final de [prompts/templates/TEMPLATE-MESTRE-VIDEO.md](prompts/templates/TEMPLATE-MESTRE-VIDEO.md). O bloco `SERIES RENDERING STYLE CONTINUITY` é obrigatório em todo prompt e nunca deve ser removido ou enfraquecido — nem mesmo como tentativa de corrigir um bloqueio do Flow; ver "Bloqueios do Flow" no template mestre.

---

## 9. Episódio 1 como referência de produção

O Episódio 1 está importado:

**S01E001 — A Greve da Patrícia**

Use:

- [episodios/S01/S01E001-A-GREVE-DA-PATRICIA.md](episodios/S01/S01E001-A-GREVE-DA-PATRICIA.md) — índice, status e consolidação;
- [episodios/S01/FONTE-HISTORICA-S01E001-A-GREVE-DA-PATRICIA.md](episodios/S01/FONTE-HISTORICA-S01E001-A-GREVE-DA-PATRICIA.md) — fonte histórica de produção.

A fonte histórica preserva como o episódio foi documentado e planejado naquela fase. Ela pode conter práticas posteriormente substituídas.

Para produzir material novo, prevalecem:

1. decisões vigentes;
2. template mestre atual;
3. aprendizados atuais;
4. continuidade atual.

Nunca reescreva silenciosamente um documento histórico para fazê-lo parecer compatível com regras posteriores.

---

## 10. Cena 2B — estudo de caso obrigatório

O repositório possui o roteiro canônico e o prompt original da Cena 2B, além de registros de erro/solução:

- [ERR-007-CENA-2B-TENTATIVA-INICIAL.md](producao/erros/ERR-007-CENA-2B-TENTATIVA-INICIAL.md)
- [SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md](producao/solucoes/SOL-007-CENA-2B-VERSAO-SIMPLIFICADA.md)

A versão revisada/aprovada **exata** que efetivamente funcionou no Flow pode permanecer `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA`.

Portanto:

- não reconstrua o prompt exato por suposição;
- não substitua automaticamente a fala canônica do roteiro por uma variante de produção;
- use os aprendizados confirmados como heurística para novos prompts.

---

## 11. Modo: criar GPT personalizado, Skill ou agente externo

Se a tarefa for criar um GPT, Skill, agente no Gemini, Claude Code, Codex ou outro sistema a partir deste repositório, **não copie todo o repositório para dentro das instruções do agente**.

A camada externa deve conter principalmente:

- papel do agente;
- tarefas permitidas;
- comportamento esperado;
- regra de consultar o repositório;
- ordem de leitura definida neste onboarding;
- obrigação de respeitar cânone e pendências;
- forma esperada de saída.

O **conhecimento do projeto deve continuar no repositório**.

### Se o agente tiver acesso contínuo ao GitHub/repositório

Use o repositório como fonte viva e consulte os arquivos conforme a tarefa.

### Se o agente NÃO tiver acesso contínuo ao GitHub

Monte um pacote de conhecimento derivado das fontes canônicas e registre explicitamente:

- repositório de origem;
- branch/ref usada;
- commit ou data do snapshot;
- arquivos incluídos;
- necessidade de atualização periódica.

Nunca trate um snapshot antigo como se fosse o estado eterno do projeto.

### Pacote mínimo recomendado para um agente sem acesso direto ao Git

Inclua, no mínimo:

- `AI-ONBOARDING.md`;
- `AGENTS.md`;
- `docs/BIBLIA-DA-SERIE.md`;
- `docs/DECISOES.md`;
- `docs/TOM-E-HUMOR.md`;
- `docs/CONTINUIDADE.md`;
- `docs/APRENDIZADOS-DE-VIDEO.md`;
- `docs/APRENDIZADOS-EM-VALIDACAO.md` quando o agente for continuar produção e precisar das hipóteses `EM TESTE`;
- `personagens/relacoes/RELACOES-FAMILIARES.md`;
- as fichas e personalidades dos personagens;
- `prompts/templates/TEMPLATE-MESTRE-VIDEO.md` quando o agente gerar vídeos;
- `producao/STATUS.md`;
- episódios relevantes para a tarefa.

---

## 12. Histórico, teste, aprovação e regra atual são coisas diferentes

Preserve sempre a distinção entre:

- **roteiro canônico** — conteúdo narrativo aprovado;
- **prompt histórico** — prompt usado em determinada etapa;
- **variante de teste** — tentativa não necessariamente aprovada;
- **erro** — falha observada;
- **solução** — correção que funcionou ou foi validada;
- **aprovação** — dimensão explicitamente aprovada;
- **aprendizado reutilizável** — regra derivada de produção;
- **regra operacional atual** — instrução vigente para material novo.

Aprovação visual não aprova automaticamente:

- voz;
- fala;
- atuação;
- personalidade;
- dinâmica narrativa.

---

## 13. Como lidar com lacunas e blockers

Consulte sempre [producao/STATUS.md](producao/STATUS.md).

Classifique uma lacuna corretamente:

### `A DEFINIR`
Ainda não existe decisão suficiente.

### `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA`
A informação já existe fora do repositório, mas a fonte ainda não foi versionada. **Não reconstruir.**

### Histórico incompleto
Preservar o que existe e indicar o que falta.

### Cenário ainda não promovido a `LOC-00X`
Isso não bloqueia automaticamente uma cena quando a ambientação necessária já estiver sustentada por episódio ou outra fonte aprovada.

---

## 14. Como escrever de volta no repositório

Uma IA com permissão de edição deve:

- preservar documentos existentes;
- não apagar histórico válido;
- não substituir silenciosamente decisões;
- separar teste de aprovação;
- registrar observações e hipóteses ainda não validadas em `docs/APRENDIZADOS-EM-VALIDACAO.md`, e não promovê-las a `docs/APRENDIZADOS-DE-VIDEO.md`, `docs/DECISOES.md` ou ao template mestre antes de `VALIDADO`;
- registrar mudanças de cânone em `docs/DECISOES.md` quando aplicável;
- atualizar `docs/CHANGELOG-CRIATIVO.md` para mudanças relevantes;
- atualizar `producao/STATUS.md` quando o estado do projeto mudar;
- registrar erros/soluções/testes em `producao/`;
- não fazer push remoto sem autorização explícita quando [AGENTS.md](AGENTS.md) exigir essa aprovação.

Evite duplicar regras completas em vários arquivos. Quando uma fonte de verdade já existir, prefira **referenciar** essa fonte.

---

## 15. Checklist antes de entregar qualquer resultado

Antes de responder, criar cena, roteiro, prompt, Skill ou agente, confirme:

- [ ] Li `AGENTS.md` e este onboarding?
- [ ] Consultei a Bíblia e decisões relevantes?
- [ ] Estou usando os Character IDs corretos?
- [ ] Li personalidade e relações dos personagens envolvidos?
- [ ] Consultei a continuidade?
- [ ] Estou respeitando a precedência de decisões e supersessões?
- [ ] Estou confundindo histórico com regra atual?
- [ ] Estou inventando algo marcado `A DEFINIR` ou `PENDENTE DE IMPORTAÇÃO`?
- [ ] Para vídeo, usei o template mestre vigente?
- [ ] Consultei aprendizados, erros e soluções relevantes?
- [ ] Minha saída contradiz alguma aprovação já registrada?
- [ ] Estou criando uma segunda fonte de verdade desnecessária?

Se qualquer resposta importante for incerta, reporte a incerteza antes de criar novo cânone.

---

## 16. Teste de onboarding para uma IA nova

Antes de se declarar pronta para trabalhar de forma autônoma no projeto, a IA deve conseguir responder corretamente, usando apenas o repositório:

1. Quem são os sete personagens e quais são seus Character IDs?
2. Quem é Sr. Antônio e por que o nome técnico legado não o torna membro da Família Silva?
3. Quais são as relações familiares principais?
4. Onde estão as sete personalidades canônicas?
5. Qual é o rendering canônico vigente?
6. Qual documento é a única fonte executável para novos prompts de vídeo?
7. Como deve tratar duração em segundos em novos prompts?
8. Qual a diferença entre o documento histórico do Episódio 1 e a regra operacional atual?
9. O que aconteceu no caso da Cena 2B e o que ainda está pendente?
10. Qual documento mostra o status atual do projeto?
11. Como resolver conflitos entre decisões sem olhar apenas para número/data?
12. O que significa `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA`?
13. Quais informações ela está proibida de inventar?
14. Como deve estruturar um GPT/Skill externo sem duplicar o repositório inteiro?

Se não conseguir responder esses pontos com evidência documental, **a IA ainda não está onboarded**.

---

## 17. Critério de sucesso

O onboarding está funcionando quando uma nova IA consegue:

- navegar sozinha pelas fontes corretas;
- compreender a Família Silva sem depender de conversas antigas;
- não reinventar decisões já tomadas;
- não confundir histórico com regra atual;
- gerar cena, roteiro ou prompt coerente com o cânone;
- reconhecer o que ainda está pendente;
- criar agentes externos que usem o repositório como conhecimento vivo;
- registrar novos aprendizados sem degradar a fonte de verdade.

**O repositório deve permanecer a fonte de verdade. O agente é apenas a camada de comportamento sobre essa fonte.**
