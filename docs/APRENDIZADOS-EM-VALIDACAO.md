# Aprendizados em Validação

**Status do documento:** `CAMADA INTERMEDIÁRIA — NÃO É CÂNONE`

Este arquivo é a camada entre **observações feitas durante a produção** e as **regras oficiais consolidadas** do projeto.

Ele existe para preservar hipóteses e observações que ainda precisam de mais teste, **sem**:

1. depender da memória ou do contexto de uma conversa com IA;
2. promover uma hipótese a regra oficial cedo demais;
3. perder o histórico de como uma regra foi descoberta;
4. misturar conhecimento validado com observação ainda experimental.

Aplica a disciplina já aprovada pela [DEC-019](DECISOES.md#dec-019) e repetida em [AGENTS.md](../AGENTS.md), no [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md) e em [LRN-023](APRENDIZADOS-DE-VIDEO.md#lrn-023--não-registrar-hipótese-como-regra-antes-de-validar):

`OBSERVAÇÃO → HIPÓTESE → EM TESTE → VALIDADO ou REJEITADO → decisão/template`

---

## Índice operacional — estado atual dos experimentos

Tabela de recuperação rápida para qualquer sessão/agente. É **índice**, não substitui a descrição completa de cada entrada mais abaixo. `EM TESTE` = experimental, **não** é regra oficial.

| ID | Resumo | Status | Origem | Evidência atual | Próximo teste | Destino provável |
| --- | --- | --- | --- | --- | --- | --- |
| [AV-001](#av-001--menos-coreografia-mais-intenção) | Descrever intenção emocional > coreografar microexpressões | `EM TESTE` | Rodada Ep. 2 (`2026-08-30`) | Cenas da rodada; regeneração da Cena 4 é o caso mais claro; causa não isolada | Mesmo beat com/sem microexpressão coreografada, mesmas refs; repetir com outra emoção/personagem | `LRN` em APRENDIZADOS-DE-VIDEO + nota no template (consolidar com AV-006) |
| [AV-002](#av-002--câmera-observacional) | Câmera observacional aumenta naturalidade no diálogo familiar | `EM TESTE` | Rodada Ep. 2 (`2026-08-30`) | Cena 3 (avanço de câmera/naturalidade); ainda há pose em finais de cena | Cena com 3+ personagens; com ação física simultânea; testar se a pose some ao encurtar a cauda | `LRN` + nota em `SHOT, CAMERA, AND COMPOSITION` do template |
| [AV-003](#av-003--uma-troca-narrativa-completa-por-geração-curta) | Preferir um beat completo por geração curta a fragmentar em microfalas | `EM TESTE` | Rodada Ep. 2 (`2026-08-30`), gerações ~10s | Cenas em ~10s; prompts sequenciais na mesma conversa geraram continuação → arquivo maior ≠ geração única | Repetir em outras configs; medir diálogo que cabe com pausa/reação; anotar mecanismo de cada geração | `LRN` complementando LRN-015/LRN-020; nota em `NARRATIVE ARCHITECTURE` |
| [AV-004](#av-004--folga-de-atuação-dentro-da-duração) | Diálogo deve ocupar menos que o máximo aparente do clipe | `EM TESTE` | Rodada Ep. 2 (`2026-08-30`), gerações ~10s | Cena 2 utilizável, mas diálogo comprimido | Mesmo beat com fala mais curta; juntar mais casos antes de qualquer limite numérico | `LRN` complementando LRN-018; reforço em `DIALOGUE DURATION FIT` |
| [AV-005](#av-005--continuidade-de-figurino-não-é-garantida-pela-master) | MASTER ancora identidade, não garante figurino entre gerações | `EM TESTE` | Rodada Ep. 2 (`2026-08-30`) | Cena 1 e Cena 2 com MASTER idêntica, Carol com roupa diferente | Par de cenas do mesmo bloco **com** `Costume Continuity` textual; depois frame aprovado como ref.; outro personagem além da Carol | Atualização de `personagens/regras/COSTUME-CONTINUITY.md` + `LRN` (compl. LRN-005); `DEC` se virar regra dura |
| [AV-006](#av-006--explicar-o-pensamento-que-causa-a-expressão) | Explicar o pensamento que causa a expressão > ordenar a expressão facial | `EM TESTE` | Rodada Ep. 2 (`2026-08-30`), Cena 4 (1ª e 2ª geração) | 1ª geração simpática demais (`"clearly unconvinced"` insuficiente); 2ª geração melhor, ainda com pose | Repetir o padrão em outra cena/personagem/emoção; combinar com AV-007; achar benchmark de deboche da Carol | Consolidar com AV-001 num único `LRN`; nota em `EMOTIONAL PERFORMANCE AND ORALITY` |
| [AV-007](#av-007--evitar-reação-final-prolongada) | Reação silenciosa como punchline deve ser imediata, sem pose sustentada | `EM TESTE` | Rodada Ep. 2 (`2026-08-30`) | Finais de cena da rodada com tendência a pose | Mesmo beat com cauda curta vs. longa; confirmar interação com AV-002 e AV-006 | `LRN` complementando LRN-022; nota em `ACTION AND PERFORMANCE` |
| [AV-008](#av-008--continuidade-realizada-tem-precedência-operacional-sobre-roteiro-planejado) | Continuidade realizada nos vídeos aprovados tem precedência operacional sobre o roteiro planejado em conflito factual | `EM TESTE` | Rodada Ep. 2 (`2026-08-30`) | Ao continuar o Ep. 2 só pelo roteiro escrito, houve divergência com o ponto que os vídeos aprovados já haviam alcançado; a revisão dos vídeos recuperou a continuidade | Observar se o procedimento evita contradições nas próximas cenas e em futuras rodadas/episódios | `docs/CONTINUIDADE.md` e/ou `docs/GUIA-DE-PRODUCAO.md`; `LRN`/`DEC` se a governança justificar |

> **Origem comum de AV-001 a AV-008:** rodada de produção do **Episódio 2**, registrada em `2026-08-30` a partir do relato de produção do usuário. Nesta data **não existe documento de episódio `S01E002` versionado** no repositório; quando existir, vincular as cenas citadas a ele. Os arquivos de vídeo desta rodada **não estão versionados** — as entradas citam apenas "Cena 1" a "Cena 4" conforme descritas pelo usuário, sem nome de arquivo, ID de clipe ou hash.

---

## Relação com os outros documentos

| Documento | Papel | Este arquivo |
| --- | --- | --- |
| [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md) | conhecimento **consolidado** de produção (`LRN-0XX`) | recebe um `LRN` **só depois** que uma entrada daqui é `VALIDADO` e promovida |
| [DECISOES.md](DECISOES.md) | decisões **permanentes** (`DEC-0XX`) | recebe uma `DEC` só quando a regra se torna permanente |
| [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md) | única fonte executável de novos prompts | **nunca** recebe um aprendizado que ainda esteja nesta camada |
| [CONTINUIDADE.md](CONTINUIDADE.md), [GUIA-DE-PRODUCAO.md](GUIA-DE-PRODUCAO.md) | estado narrativo e fluxo de trabalho | podem receber uma regra promovida daqui (ex.: destino provável de [AV-008](#av-008--continuidade-realizada-tem-precedência-operacional-sobre-roteiro-planejado)) |
| [producao/testes/](../producao/testes/), [producao/erros/](../producao/erros/), [producao/solucoes/](../producao/solucoes/) | evidência bruta por geração | são a **fonte de evidência** citada nas entradas daqui |

Regra de subida: **uma descoberta experimental entra primeiro aqui.** Só sobe para `APRENDIZADOS-DE-VIDEO.md`, `DECISOES.md`, uma regra em `personagens/regras/`, `CONTINUIDADE.md`, `GUIA-DE-PRODUCAO.md` ou `TEMPLATE-MESTRE-VIDEO.md` quando a evidência for suficiente (ver [Força da evidência](#força-da-evidência)).

> Uma IA que assumir uma nova sessão de produção **deve ler este arquivo** para recuperar as hipóteses atualmente `EM TESTE` antes de gerar cena, prompt ou vídeo novo. Ver [Recuperação de contexto por uma nova IA](#recuperação-de-contexto-por-uma-nova-ia). Ele consta da ordem de leitura em [AI-ONBOARDING.md](../AI-ONBOARDING.md).

## O que entra e o que não entra

**Entra:**

- observação de produção que sugere uma regra, mas ainda não foi confirmada;
- hipótese sobre comportamento de ferramenta, prompt, atuação, câmera, continuidade;
- regra provisória adotada "por enquanto" enquanto se junta evidência (registrada no campo `Decisão operacional atual`).

**Não entra:**

- fato já consolidado (vai direto para o documento oficial pela via normal);
- invenção de característica, relação, figurino, voz, cena ou ID de personagem — continua proibido por [AGENTS.md](../AGENTS.md);
- nome de arquivo de vídeo, ID, hash ou caminho que não possa ser comprovado no repositório;
- evidência que não existe. Se não há cena que sustente a observação, não registrar.

## Estados — experimental vs. regra oficial

Os quatro primeiros estados são **experimentais**: a entrada **não é cânone** e não deve ser tratada como regra fechada. Só `PROMOVIDO` significa que o conhecimento virou regra oficial — e, mesmo aí, a regra vigente é a do **documento de destino**, não esta entrada.

| Estado | Definição | É regra oficial? |
| --- | --- | --- |
| `HIPÓTESE` | observação ainda não suficientemente testada | não |
| `EM TESTE` | hipótese com experimento/evidência em andamento | não |
| `VALIDADO` | evidência considerada suficiente para **iniciar o processo de promoção** | não |
| `REJEITADO` | hipótese não sustentada pelas evidências | não (fica como histórico) |
| `PROMOVIDO` | conhecimento já incorporado à documentação oficial | sim — na regra de destino |

**Importante:**

- `VALIDADO` **não significa automaticamente que o Template Mestre foi alterado**, nem que qualquer documento oficial mudou. Significa apenas que a evidência já basta para começar a promover.
- `PROMOVIDO` **deve indicar explicitamente para onde** o conhecimento foi incorporado — ver os campos `Promovido para`, `Data da promoção` e `LRN/DEC/regra relacionada` na [Trilha de promoção](#trilha-de-promoção).
- Uma entrada `VALIDADO` que ainda não foi promovida continua `VALIDADO` até que alguém faça a promoção e a marque como `PROMOVIDO`.
- Uma entrada `REJEITADO` **não é apagada** — o histórico da tentativa é aprendizado.

### Decisão operacional provisória ≠ regra canônica validada

O campo `Decisão operacional atual` de cada entrada responde: *"enquanto esta hipótese ainda está sendo testada, o que estamos fazendo na produção?"*

Uma decisão operacional provisória pode ser adotada mesmo antes da validação quando o **custo é baixo e o risco de não fazer é alto** (exemplo: declarar `Costume Continuity` explicitamente por causa de [AV-005](#av-005--continuidade-de-figurino-não-é-garantida-pela-master)). Isso **não** transforma a hipótese em cânone, não altera o Template Mestre e não dispensa a validação. É uma escolha de produção reversível, não uma regra permanente.

## Processo de governança

```text
OBSERVAÇÃO
  └─ registrada numa geração real (producao/testes, producao/erros)
        │
        ▼
HIPÓTESE                     entrada criada aqui, com ID AV-0XX
        │
        ▼
EM TESTE                     novas cenas/rodadas geram evidência
        │                    (decisão operacional provisória pode ser adotada aqui)
        ▼
evidência acumulada          avaliada pela "Força da evidência", não por contagem fixa
        │
        ├─────────────► REJEITADO   (contradição ou explicação alternativa melhor)
        │
        ▼
VALIDADO                     evidência suficiente para iniciar a promoção
        │                    (o Template Mestre ainda NÃO foi alterado)
        ▼
promover para o documento oficial apropriado
  (APRENDIZADOS-DE-VIDEO.md / DECISOES.md / personagens/regras/ /
   CONTINUIDADE.md / GUIA-DE-PRODUCAO.md /
   e só então, se for o caso, TEMPLATE-MESTRE-VIDEO.md)
        │
        ▼
marcar a entrada original como PROMOVIDO
  e preencher Promovido para / Data da promoção / LRN-DEC-regra relacionada
```

### Força da evidência

**Não existe regra de "sempre três testes".** Uma observação forte e inequívoca pode ser validada rápido; uma observação sutil sobre comportamento de ferramenta pode exigir muitas rodadas. O campo `Nº de confirmações` é informação de contexto, **não** um critério mecânico. Avaliar:

- **Repetibilidade** — o efeito reaparece quando a mudança é aplicada de novo?
- **Diversidade de contexto** — aparece em cenas, personagens, emoções e configurações diferentes, ou só num caso?
- **Clareza da relação causa/efeito** — a mudança testada explica o resultado, ou há muitas variáveis juntas?
- **Ausência de explicação alternativa** — existe outra causa igualmente plausível não descartada?
- **Impacto do comportamento** — quanto muda o resultado final? Efeitos grandes merecem mais cuidado antes de virar regra dura.

Registrar sempre a **separação entre fato observado e interpretação causal** (disciplina de [AGENTS.md](../AGENTS.md) e [LRN-023](APRENDIZADOS-DE-VIDEO.md#lrn-023--não-registrar-hipótese-como-regra-antes-de-validar)).

### Trilha de promoção

Cada entrada carrega estes campos para tornar a promoção rastreável:

- **Destino provável:** onde o aprendizado deve ser incorporado se validado (preenchido desde o início).
- **Promovido para:** documento e seção exatos onde a regra final foi escrita (`—` enquanto não promovido).
- **Data da promoção:** `AAAA-MM-DD` ou `—`.
- **LRN/DEC/regra relacionada:** o identificador final que passou a valer (`LRN-0XX`, `DEC-0XX`, arquivo em `personagens/regras/`, seção de `CONTINUIDADE.md`…), ou `—`.

O `AV-0XX` **não precisa** manter o mesmo número do futuro `LRN`/`DEC`. Ele apenas registra o link para o destino.

### Como promover

1. Confirmar que a entrada está `VALIDADO` pelos critérios de [Força da evidência](#força-da-evidência).
2. Escrever o aprendizado no documento oficial certo:
   - heurística de produção reutilizável → novo `LRN-0XX` em [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md);
   - regra permanente de cânone/processo → nova `DEC-0XX` em [DECISOES.md](DECISOES.md);
   - regra de continuidade visual → arquivo em [personagens/regras/](../personagens/regras/);
   - regra de continuidade narrativa ou de fluxo → [CONTINUIDADE.md](CONTINUIDADE.md) / [GUIA-DE-PRODUCAO.md](GUIA-DE-PRODUCAO.md);
   - e **só depois de consolidada**, ajuste correspondente no [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
3. Atualizar [CHANGELOG-CRIATIVO.md](CHANGELOG-CRIATIVO.md) e [producao/STATUS.md](../producao/STATUS.md) quando houver impacto.
4. Voltar aqui, mudar o status para `PROMOVIDO` e preencher `Promovido para`, `Data da promoção` e `LRN/DEC/regra relacionada`.

## Convenção de ID

- Formato: `AV-0XX` (`A`prendizado em `V`alidação), sequencial, três dígitos, permanente.
- O ID não é reaproveitado nem renumerado. Quando promovido, ele **não vira** o número do `LRN`/`DEC` de destino; a entrada `AV` apenas registra o link.
- Registrado também em [NOMENCLATURA.md](NOMENCLATURA.md).

## Template de entrada

```text
### AV-0XX — [título curto]

- **Data:** AAAA-MM-DD
- **Origem / rodada de produção:** [rodada, episódio se houver documento versionado, ferramenta]
- **Hipótese ou observação:** [o que se está afirmando provisoriamente]
- **Problema que motivou o teste:** [o que estava ruim ou incerto]
- **Mudança testada:** [o que foi alterado no prompt / método / referência]
- **Evidências / cenas:** [cenas reais que sustentam; sem inventar arquivo, ID ou hash]
- **Resultado observado:** [fato observado, separado de interpretação]
- **Nº de confirmações:** [quantas rodadas/cenas independentes; contexto, não critério mecânico]
- **Status:** HIPÓTESE | EM TESTE | VALIDADO | REJEITADO | PROMOVIDO
- **Decisão operacional atual:** [o que a produção faz ENQUANTO isto está EM TESTE; provisório, reversível, não é cânone]
- **Próximos testes necessários:** [o que ainda falta para validar ou rejeitar]
- **Destino provável:** [qual documento oficial deve receber se validado]
- **Promovido para:** [documento + seção exatos, ou —]
- **Data da promoção:** [AAAA-MM-DD ou —]
- **LRN/DEC/regra relacionada:** [identificador final que passou a valer, ou —]
- **Observações:** [ressalvas, links, relação com outros AV/LRN/DEC]
```

---

# Entradas

---

### AV-001 — Menos coreografia, mais intenção

- **Data:** `2026-08-30`
- **Origem / rodada de produção:** rodada do Episódio 2; ferramenta de vídeo da rodada (relato de produção).
- **Hipótese ou observação:** para a Família Silva, **descrever a intenção emocional** do personagem tende a produzir atuação mais natural do que **coreografar microexpressões** (pausas, olhares, sorrisos, movimentos de sobrancelha).
- **Problema que motivou o teste:** prompts que detalhavam demais microexpressões produziram atuação artificial, com sensação de personagens "executando instruções".
- **Mudança testada:** reescrever a direção de atuação para descrever principalmente o **estado/intenção emocional**, deixando o modelo interpretar a expressão facial.
- **Evidências / cenas:** cenas da rodada do Episódio 2 em que a direção passou de microexpressões detalhadas para intenção; a regeneração da Cena 4 (ver [AV-006](#av-006--explicar-o-pensamento-que-causa-a-expressão)) é o caso mais claro.
- **Resultado observado:** resultados descritos como mais naturais quando o prompt priorizou intenção. **Interpretação causal ("é a coreografia que artificializa") ainda não isolada** — os prompts mudaram em mais de um aspecto ao mesmo tempo.
- **Nº de confirmações:** 1 rodada de produção; sinais convergentes em mais de uma cena da mesma rodada.
- **Status:** `EM TESTE`
- **Decisão operacional atual:** nos próximos prompts, descrever a **intenção emocional de forma clara e específica** e evitar coreografar microexpressão por microexpressão. A direção emocional continua obrigatória — não "remover emoção", e sim parar de roteirizar cada músculo do rosto. Provisório; não é cânone.
- **Próximos testes necessários:** isolar a variável — mesmo beat, um prompt com microexpressões coreografadas e outro só com intenção, mesmas referências e configuração; repetir com personagem e emoção diferentes.
- **Destino provável:** novo `LRN` em [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md), consolidado com [AV-006](#av-006--explicar-o-pensamento-que-causa-a-expressão), e nota nas seções `ACTION AND PERFORMANCE` / `EMOTIONAL PERFORMANCE AND ORALITY` do [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- **Promovido para:** —
- **Data da promoção:** —
- **LRN/DEC/regra relacionada:** —
- **Observações:** **não** significa remover direção emocional. Relacionado a [AV-006](#av-006--explicar-o-pensamento-que-causa-a-expressão) (mesmo princípio) e a `LRN-019` (linguagem falada e emoção específica); ao promover, **consolidar AV-001 e AV-006 num único aprendizado**, sem duplicar regra.

---

### AV-002 — Câmera observacional

- **Data:** `2026-08-30`
- **Origem / rodada de produção:** rodada do Episódio 2; ferramenta de vídeo da rodada (relato de produção).
- **Hipótese ou observação:** para diálogos familiares, uma **câmera observacional e discreta**, como testemunha da conversa, tende a aumentar a naturalidade.
- **Problema que motivou o teste:** cenas em que os personagens pareciam atuar/apresentar **para a câmera** em vez de conversar entre si.
- **Mudança testada:** direcionar o prompt para os personagens conversarem entre si, com a câmera posicionada como observadora, sem endereçamento à lente.
- **Evidências / cenas:** cenas da rodada do Episódio 2, com destaque para a Cena 3 (avanço em naturalidade/câmera).
- **Resultado observado:** cenas descritas como melhores com esse enquadramento. **Ainda há tendência a pose/performance em certos finais de cena** — ver [AV-007](#av-007--evitar-reação-final-prolongada).
- **Nº de confirmações:** 1 rodada de produção.
- **Status:** `EM TESTE`
- **Decisão operacional atual:** nas próximas cenas de diálogo, posicionar a câmera como observadora discreta e orientar os personagens a conversarem entre si, não com a lente. **Não** fixar "câmera sempre parada" nem proibir movimento — só evitar o endereçamento à câmera. Provisório.
- **Próximos testes necessários:** confirmar em cena com 3+ personagens; verificar se o ganho se mantém quando há ação física simultânea; testar se o efeito de pose no final some ao encurtar a cauda da cena.
- **Destino provável:** `LRN` em [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md) e nota na seção `SHOT, CAMERA, AND COMPOSITION` do [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- **Promovido para:** —
- **Data da promoção:** —
- **LRN/DEC/regra relacionada:** —
- **Observações:** manter `EM TESTE` justamente pela deriva de pose nos finais. Não transformar em regra dura de "sempre câmera parada".

---

### AV-003 — Uma troca narrativa completa por geração curta

- **Data:** `2026-08-30`
- **Origem / rodada de produção:** rodada do Episódio 2, trabalhando com gerações de **10 segundos**; ferramenta de vídeo da rodada (relato de produção).
- **Hipótese ou observação:** quando o volume de diálogo permitir, preferir **um pequeno beat narrativo completo** por geração em vez de fragmentar em microfalas artificiais.
- **Problema que motivou o teste:** fragmentação excessiva do diálogo em microfalas produziu resultado narrativo pior do que uma troca curta e completa.
- **Mudança testada:** escrever o prompt como **uma troca de diálogo curta e completa** dentro da geração, em vez de dividir a mesma conversa em vários clipes.
- **Evidências / cenas:** cenas da rodada do Episódio 2 geradas em janelas de ~10s.
- **Resultado observado:** troca curta e completa deu melhor resultado narrativo. **Contexto operacional:** ao usar dois prompts em sequência na mesma conversa da ferramenta, houve **continuação** que resultou em arquivo maior — **não inferir que o arquivo maior representa uma única geração nativa** (mesma ressalva de `LRN-015`/[DEC-018](DECISOES.md#dec-018)).
- **Nº de confirmações:** 1 rodada de produção.
- **Status:** `EM TESTE`
- **Decisão operacional atual:** quando o volume de diálogo couber, escrever a cena como **uma troca curta e completa** dentro de uma geração; anotar em cada geração se foi geração única, extensão, continuação ou sequência. **Não** tratar `10s` como padrão da série. Provisório.
- **Próximos testes necessários:** confirmar em outras rodadas e configurações; medir quanto diálogo cabe de fato numa geração curta com pausa e reação (ver [AV-004](#av-004--folga-de-atuação-dentro-da-duração)); registrar explicitamente, a cada geração, o mecanismo real.
- **Destino provável:** `LRN` em [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md) complementando `LRN-015` e `LRN-020`; eventual nota em `NARRATIVE ARCHITECTURE` no [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- **Promovido para:** —
- **Data da promoção:** —
- **LRN/DEC/regra relacionada:** —
- **Observações:** **não generalizar `10s` como regra universal** de todas as ferramentas/configurações. É o beat que manda, não a duração (`LRN-020`).

---

### AV-004 — Folga de atuação dentro da duração

- **Data:** `2026-08-30`
- **Origem / rodada de produção:** rodada do Episódio 2, gerações de ~10s; ferramenta de vídeo da rodada (relato de produção).
- **Hipótese ou observação:** o diálogo deve ocupar **menos que a capacidade máxima aparente** do clipe, deixando espaço natural para respiração, reação e timing.
- **Problema que motivou o teste:** a Cena 2 ficou utilizável, mas o diálogo ocupou praticamente toda a duração e pareceu **comprimido**.
- **Mudança testada:** ainda em teste — a regra provisória adotada é: **se for necessário acelerar artificialmente a fala para caber, encurtar o diálogo.**
- **Evidências / cenas:** Cena 2 da rodada do Episódio 2 (aprovada para continuidade, com diálogo comprimido).
- **Resultado observado:** diálogo no limite da duração → sensação de compressão, mesmo com a cena aproveitável.
- **Nº de confirmações:** 1 cena.
- **Status:** `EM TESTE`
- **Decisão operacional atual:** dimensionar a fala com folga dentro da janela real; **se precisar acelerar artificialmente para caber, encurtar o diálogo** — isso já é consistente com [AGENTS.md](../AGENTS.md) e `LRN-018` e pode ser aplicado agora. **Não** aplicar limite numérico de caracteres ou percentual de ocupação. Provisório na parte "ocupar menos que o máximo aparente".
- **Próximos testes necessários:** gerar o mesmo beat com versão de fala mais curta e comparar respiração/reação; juntar mais casos antes de definir qualquer limite.
- **Destino provável:** `LRN` em [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md) complementando `LRN-018`; reforço na seção `DIALOGUE DURATION FIT` do [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- **Promovido para:** —
- **Data da promoção:** —
- **LRN/DEC/regra relacionada:** —
- **Observações:** o princípio de encurtar a fala já é cânone vigente. O que está `EM TESTE` é a formulação mais forte ("ocupar menos que o máximo aparente"), não o princípio.

---

### AV-005 — Continuidade de figurino não é garantida pela MASTER

- **Data:** `2026-08-30`
- **Origem / rodada de produção:** rodada do Episódio 2; ferramenta de vídeo da rodada (relato de produção).
- **Hipótese ou observação:** a imagem MASTER de personagem ancora **identidade visual**, mas **não é suficiente, sozinha, para preservar figurino entre gerações**. Cenas do mesmo bloco temporal devem declarar explicitamente `Costume Continuity`.
- **Problema que motivou o teste:** Cena 1 e Cena 2 usaram as mesmas MASTERs dos personagens, mas **Carol apareceu com diferenças de roupa** entre as gerações.
- **Mudança testada (em andamento):**
  - declarar `Costume Continuity` explícito para cenas do mesmo bloco temporal;
  - descrição textual das peças e cores aprovadas no prompt;
  - uso de **frame aprovado de cena anterior** como referência complementar de figurino, quando a ferramenta permitir.
- **Evidências / cenas:** Cena 1 e Cena 2 da rodada do Episódio 2 (deriva de figurino da Carol com MASTER idêntica).
- **Resultado observado (fato):** MASTER igual + sem `Costume Continuity` textual → figurino derivou. **Ainda não testado** se `Costume Continuity` textual sozinho resolve, nem se o frame adicional resolve.
- **Nº de confirmações:** 1 rodada (2 cenas do mesmo bloco).
- **Status:** `EM TESTE`
- **Decisão operacional atual:** nas cenas do mesmo bloco temporal, **declarar `Costume Continuity` explicitamente** e descrever as peças e cores aprovadas no prompt; usar um frame aprovado como referência complementar de figurino quando a ferramenta permitir. Justificativa: custo baixo, risco de deriva alto. **Não** declarar o problema resolvido nem afirmar que o frame adicional o resolve. Provisório.
- **Próximos testes necessários:** gerar par de cenas do mesmo bloco **com** `Costume Continuity` textual e comparar; depois testar o frame aprovado como referência complementar; verificar em outro personagem além da Carol.
- **Destino provável:** atualização de [personagens/regras/COSTUME-CONTINUITY.md](../personagens/regras/COSTUME-CONTINUITY.md), `LRN` em [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md) (complementa `LRN-005`) e, se virar regra dura, `DEC`.
- **Promovido para:** —
- **Data da promoção:** —
- **LRN/DEC/regra relacionada:** —
- **Observações:** consistente com `LRN-005` ("continuidade precisa ser explícita"); esta entrada acrescenta o ponto específico de que **a MASTER V02 não cobre figurino** e testa mecanismos de reforço.

---

### AV-006 — Explicar o pensamento que causa a expressão

- **Data:** `2026-08-30`
- **Origem / rodada de produção:** rodada do Episódio 2, Cena 4 (primeira geração e regeneração); ferramenta de vídeo da rodada (relato de produção).
- **Hipótese ou observação:** **explicar o pensamento/intenção que causa uma expressão** pode funcionar melhor do que ordenar mecanicamente a expressão facial.
- **Problema que motivou o teste:** na 1ª geração da Cena 4, Carol deveria reagir com **deboche/desconfiança**, como quem confirmou uma suspeita sobre Beto. O prompt dizia essencialmente que ela estava *"clearly unconvinced"* — insuficiente; o resultado ficou excessivamente simpático/"fofinho".
- **Mudança testada:** na regeneração, a direção passou a explicar o **estado mental**: Carol já suspeitava da resposta; a resposta evasiva de Beto **confirma** o que ela já sabia; a reação deve carregar a sensação silenciosa de *"eu sabia"*.
- **Evidências / cenas:** Cena 4 — 1ª geração (não aprovada como referência emocional) e 2ª geração (mais próxima da intenção, ainda com tendência a pose; não é benchmark definitivo).
- **Resultado observado:** descrever o estado mental aproximou o resultado do objetivo, mas **não atingiu perfeitamente** o deboche/desconfiança e ainda apresentou pose.
- **Nº de confirmações:** 1 cena, 2 gerações (comparação direta antes/depois).
- **Status:** `EM TESTE`
- **Decisão operacional atual:** ao pedir uma expressão emocional específica, **explicar no prompt o pensamento/estado mental que a causa** (o que o personagem já sabe, o que a fala do outro confirma, o que ele sente por dentro), em vez de só nomear a expressão. Na prática, aplicar junto de [AV-001](#av-001--menos-coreografia-mais-intenção). Provisório.
- **Próximos testes necessários:** repetir o padrão "explicar o pensamento" em outra cena/personagem/emoção; verificar se some a tendência a pose quando combinado com [AV-007](#av-007--evitar-reação-final-prolongada); buscar uma geração que atinja de fato o deboche para servir de benchmark da Carol.
- **Destino provável:** **consolidar com [AV-001](#av-001--menos-coreografia-mais-intenção) num único `LRN`** em [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md); nota em `EMOTIONAL PERFORMANCE AND ORALITY` no [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md). Não duplicar a regra em dois lugares.
- **Promovido para:** —
- **Data da promoção:** —
- **LRN/DEC/regra relacionada:** —
- **Observações:** a intenção "deboche/desconfiança + eu sabia" é **consistente com a personalidade canônica da Carol** ([CAROL-PERSONALIDADE.md](../personagens/oficiais/personalidades/CAROL-PERSONALIDADE.md): percepção antecipada, reação, ironia, incredulidade diante de justificativa fraca). Nenhuma personalidade foi alterada.

---

### AV-007 — Evitar reação final prolongada

- **Data:** `2026-08-30`
- **Origem / rodada de produção:** rodada do Episódio 2; ferramenta de vídeo da rodada (relato de produção).
- **Hipótese ou observação:** quando a **reação silenciosa é o punchline**, ela deve acontecer **imediatamente** como consequência da fala anterior, e a cena deve encerrar naturalmente — sem transformar a reação em pose sustentada.
- **Problema que motivou o teste:** quando há espaço excessivo depois da última fala, ou quando se pede uma "reação final prolongada", o personagem começa a parecer que está **posando para a câmera**.
- **Mudança testada (em andamento):** encurtar a cauda da cena depois da última fala; pedir a reação como consequência imediata, não como plano sustentado.
- **Evidências / cenas:** finais de cena da rodada do Episódio 2 com tendência a pose (relacionado à ressalva de [AV-002](#av-002--câmera-observacional) e à 2ª geração da Cena 4 em [AV-006](#av-006--explicar-o-pensamento-que-causa-a-expressão)).
- **Resultado observado:** cauda longa / pedido de reação prolongada → aparência de pose.
- **Nº de confirmações:** observado em mais de uma cena da mesma rodada.
- **Status:** `EM TESTE`
- **Decisão operacional atual:** quando a reação silenciosa é o punchline, **encerrar a cena logo após a última fala** e pedir a reação como consequência imediata; **não** pedir "reação final prolongada" nem deixar cauda longa depois da fala. Provisório.
- **Próximos testes necessários:** gerar o mesmo beat com cauda curta vs. cauda longa e comparar a sensação de pose; confirmar interação com [AV-002](#av-002--câmera-observacional) e [AV-006](#av-006--explicar-o-pensamento-que-causa-a-expressão).
- **Destino provável:** `LRN` em [APRENDIZADOS-DE-VIDEO.md](APRENDIZADOS-DE-VIDEO.md) complementando `LRN-022` (payoff silencioso); nota em `ACTION AND PERFORMANCE` no [TEMPLATE-MESTRE-VIDEO.md](../prompts/templates/TEMPLATE-MESTRE-VIDEO.md).
- **Promovido para:** —
- **Data da promoção:** —
- **LRN/DEC/regra relacionada:** —
- **Observações:** `LRN-022` já diz que o payoff silencioso pode ser mais forte que fala explicativa; esta entrada acrescenta **como filmar esse payoff** (timing imediato, sem pose sustentada).

---

### AV-008 — Continuidade realizada tem precedência operacional sobre roteiro planejado

- **Data:** `2026-08-30`
- **Origem / rodada de produção:** rodada do Episódio 2; ferramenta de vídeo da rodada (relato de produção).
- **Hipótese ou observação:** quando houver **conflito factual** entre o roteiro planejado e o material audiovisual já aprovado, a próxima cena de uma sequência em produção deve partir prioritariamente da **continuidade efetivamente realizada nos vídeos aprovados**.
- **Problema que motivou o teste:** durante a produção do Episódio 2, o roteiro escrito inicial foi sendo ajustado na prática — falas reescritas, beats originalmente separados condensados, cenas passando a cumprir funções narrativas diferentes das previstas. Ao tentar **continuar o Episódio 2 usando apenas o roteiro escrito**, houve divergência em relação ao ponto narrativo que os vídeos já aprovados haviam realmente alcançado.
- **Mudança testada:** revisar os vídeos aprovados para recuperar a continuidade realizada e reconciliá-la com o roteiro antes de escrever a próxima cena.
- **Evidências / cenas:** rodada de produção do Episódio 2 em `2026-08-30`. A revisão dos vídeos aprovados permitiu recuperar corretamente a continuidade realizada. Nenhum arquivo de vídeo, hash ou ID está versionado no repositório para esta rodada.
- **Resultado observado:** partir só do roteiro escrito gerou divergência de continuidade; revisar o material aprovado corrigiu o ponto de partida.
- **Nº de confirmações:** 1 rodada de produção.
- **Status:** `EM TESTE`
- **Decisão operacional atual:** antes de gerar a próxima cena de uma sequência em andamento, **verificar o último material aprovado disponível e reconciliá-lo com o roteiro planejado**. Em conflito factual (fala, figurino, relação espacial, estado emocional, acontecimento), a **continuidade realizada prevalece** para o ponto de partida da próxima cena. O roteiro continua orientando o **arco futuro**. Provisório.
- **Próximos testes necessários:** observar se esse procedimento evita contradições narrativas nas próximas cenas do Episódio 2 e em futuras rodadas/episódios; registrar cada caso em que roteiro e material aprovado divergiram e como foram reconciliados.
- **Destino provável:** [docs/CONTINUIDADE.md](CONTINUIDADE.md) e/ou [docs/GUIA-DE-PRODUCAO.md](GUIA-DE-PRODUCAO.md); pode gerar `LRN` ou `DEC` se a governança existente justificar.
- **Promovido para:** —
- **Data da promoção:** —
- **LRN/DEC/regra relacionada:** —
- **Observações:** **não** significa que o roteiro deixa de ser fonte de planejamento. Separar sempre:
  - **ROTEIRO PLANEJADO** = intenção narrativa e estrutura prevista;
  - **CONTINUIDADE REALIZADA** = fatos, falas, figurinos, relações espaciais, estados emocionais e acontecimentos que efetivamente aparecem no material aprovado.

  O roteiro deve ser **reconciliado** com o que já foi estabelecido na tela, não descartado. Alinhado ao princípio de [AGENTS.md](../AGENTS.md) de que documento histórico preserva o método da época e não substitui a regra vigente, e à distinção de [AI-ONBOARDING.md](../AI-ONBOARDING.md) entre roteiro canônico, prompt histórico e regra atual. Relaciona-se a `LRN-021` (compressão narrativa preserva a fonte histórica) e à tabela de eventos de [CONTINUIDADE.md](CONTINUIDADE.md).

---

## Status das cenas da rodada do Episódio 2

Registro do estado de cada cena **conforme relatado pelo usuário em `2026-08-30`**. Não há arquivo de vídeo, ID de clipe ou hash versionado para esta rodada; a lista abaixo é histórico de produção, não aprovação formal em [producao/aprovados/](../producao/aprovados/).

| Cena | Estado relatado | Observação |
| --- | --- | --- |
| Cena 1 | referência inicial de naturalidade desta rodada | aprovada como benchmark de naturalidade da rodada |
| Cena 2 | utilizável / aprovada para continuidade | diálogo comprimido ([AV-004](#av-004--folga-de-atuação-dentro-da-duração)) e deriva de figurino ([AV-005](#av-005--continuidade-de-figurino-não-é-garantida-pela-master)) |
| Cena 3 | avanços em naturalidade / câmera; usada como evidência adicional | ainda com ajustes finos necessários ([AV-002](#av-002--câmera-observacional)) |
| Cena 4 — 1ª geração | **não** aprovada como referência emocional | reação final da Carol ficou simpática demais; não comunicou deboche/desconfiança ([AV-006](#av-006--explicar-o-pensamento-que-causa-a-expressão)) |
| Cena 4 — 2ª geração | melhor que a primeira, mais próxima da intenção | ainda não é benchmark definitivo da expressão da Carol; ainda apresenta pose |

---

## Recuperação de contexto por uma nova IA

Ordem lógica para uma IA que entra no projeto **durante uma produção em andamento**:

a) ler o cânone e a documentação oficial na ordem de [AI-ONBOARDING.md](../AI-ONBOARDING.md) (seção 3) e as regras de [AGENTS.md](../AGENTS.md);
b) ler **este arquivo** (`APRENDIZADOS-EM-VALIDACAO.md`) — começar pelo [Índice operacional](#índice-operacional--estado-atual-dos-experimentos);
c) identificar quais `AV` `EM TESTE` são relevantes para a tarefa e ler as entradas completas correspondentes, incluindo o campo `Decisão operacional atual`;
d) consultar o roteiro e a continuidade planejada do episódio/cena ([docs/CONTINUIDADE.md](CONTINUIDADE.md), episódio correspondente);
e) quando já existir **sequência audiovisual produzida e disponível**, verificar o estado **realmente realizado** no último material aprovado antes de continuar, e reconciliá-lo com o roteiro — ver [AV-008](#av-008--continuidade-realizada-tem-precedência-operacional-sobre-roteiro-planejado);
f) **não** transformar automaticamente um `AV` em regra oficial; seguir a [Trilha de promoção](#trilha-de-promoção) só quando a evidência justificar.

## Procedimento para novas entradas

1. Registrar a observação numa geração real em [producao/testes/](../producao/testes/) (e [producao/erros/](../producao/erros/) se houver defeito).
2. Criar aqui a entrada `AV-0XX` com o [template](#template-de-entrada), status inicial `HIPÓTESE` ou `EM TESTE`, e adicionar uma linha no [Índice operacional](#índice-operacional--estado-atual-dos-experimentos).
3. A cada nova cena/rodada que toque a hipótese, atualizar **Resultado observado**, **Nº de confirmações**, **Decisão operacional atual** e **Próximos testes necessários** (e a linha do índice).
4. Quando a [Força da evidência](#força-da-evidência) for suficiente, mudar para `VALIDADO`.
5. Promover ([Como promover](#como-promover)), mudar para `PROMOVIDO` e preencher `Promovido para`, `Data da promoção` e `LRN/DEC/regra relacionada`.
6. Se a evidência contradisser a hipótese, mudar para `REJEITADO` e registrar o porquê — sem apagar a entrada.
