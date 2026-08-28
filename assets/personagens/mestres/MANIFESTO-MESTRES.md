# MANIFESTO DE IMAGENS MESTRE

As imagens abaixo foram versionadas neste repositório em `2026-08-27` (commit original `dd9ee76`, importado para o canon consolidado em `2026-08-28` pela [DEC-014](../../docs/DECISOES.md#dec-014)). A imagem mestre é a fonte visual primária de identidade de cada personagem. Os arquivos originais foram preservados na origem indicada.

| ID | Nome | Arquivo mestre | Versão | Formato | Dimensões | SHA-256 | Arquivo original | Origem | Data de ingestão | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `CHAR-001` | Marcos Silva | `IMG-CHAR-001-MARCOS-MASTER-V01.jpeg` | `V01` | `JPEG` | `768x1376` | `4266C99B782DAAAF333080357F5CFAE11CA6B4B042A1BD751DBB53A04EF9474D` | `marcos_silva.jpeg` | `C:\Users\vanze\Área de Trabalho\familia_silva` | `2026-08-27` | `MASTER VERSIONADA` |
| `CHAR-002` | Dona Célia | `IMG-CHAR-002-DONA-CELIA-MASTER-V01.png` | `V01` | `PNG` | `1024x1536` | `D1C2E741ABB8439C93CDAEA223CF9F0C29E94CC14F9E9D9A9D37880C57E0EB3D` | `celia_silva.png` | `C:\Users\vanze\Área de Trabalho\familia_silva` | `2026-08-27` | `MASTER VERSIONADA` |
| `CHAR-003` | Patrícia Silva | `IMG-CHAR-003-PATRICIA-SILVA-MASTER-V01.png` | `V01` | `PNG` | `1024x1536` | `3192A9BEF50D75FBF40D247ACFF36CA2F533FDAA08A6BD6759E23377D28F029D` | `patricia_silva.png` | `C:\Users\vanze\Área de Trabalho\familia_silva` | `2026-08-27` | `MASTER VERSIONADA — ver nota de reconciliação abaixo` |
| `CHAR-004` | Sr. Antônio (nome de arquivo legado: Antônio Silva) | `IMG-CHAR-004-ANTONIO-SILVA-MASTER-V01.png` | `V01` | `PNG` | `1024x1536` | `FFF5E63F6360A2B1FF26DDD62ECDCE70CF4ACDE21AE7307F2FB6A33903C4FACD` | `antonio_silva.png` | `C:\Users\vanze\Área de Trabalho\familia_silva` | `2026-08-27` | `MASTER VERSIONADA` |
| `CHAR-005` | Beto | `IMG-CHAR-005-BETO-MASTER-V01.png` | `V01` | `PNG` | `1024x1536` | `C91167786B7F20642F9E17251DE8C3A73A3620041E0B3D167F22BA6D723FA786` | `beto.png` | `C:\Users\vanze\Área de Trabalho\familia_silva` | `2026-08-27` | `MASTER VERSIONADA` |
| `CHAR-006` | Carol Silva | `IMG-CHAR-006-CAROL-SILVA-MASTER-V01.png` | `V01` | `PNG` | `1024x1536` | `F9DA7325FC89274F1048E528227291600B8D005623EA4919B43414377DC0531D` | `carol_silva.png` | `C:\Users\vanze\Área de Trabalho\familia_silva` | `2026-08-27` | `MASTER VERSIONADA` |
| `CHAR-007` | Dudu Silva | `IMG-CHAR-007-DUDU-SILVA-MASTER-V01.png` | `V01` | `PNG` | `1024x1536` | `55A47615B784D1977D68AD13539ED1D35DC488F451DE784B0A77AB105045A42D` | `dudu_silva.png` | `C:\Users\vanze\Área de Trabalho\familia_silva` | `2026-08-27` | `MASTER VERSIONADA — ver ERR-006 sobre necessidade de referência neutra adicional` |

## Nota de reconciliação — `2026-08-28`

Estes sete arquivos existiam desde `2026-08-27` (commit `dd9ee76`), mas nunca haviam sido enviados a `origin/main`; por isso as fichas de personagem geradas em `origin/main` em `2026-08-28` os descreviam como "ainda não versionados em assets/". Esta reconciliação importa os arquivos físicos, resolvendo essa pendência específica em todas as fichas.

## Nota sobre Patrícia (`CHAR-003`) — `BLOCKED_BY_HUMAN_DECISION`

O arquivo `IMG-CHAR-003-PATRICIA-SILVA-MASTER-V01.png` corresponde à interpretação visual original ("V01"), registrada no repositório desde `2026-08-27` como `LEGACY / SUPERSEDED VISUALLY` frente a uma nova interpretação aprovada posteriormente (estilo mais realista, corpo mais esguio, blusa terracota) cujo arquivo definitivo (`V02`) nunca foi fornecido. A ficha de Patrícia gerada em `origin/main` em `2026-08-28` rotula sua referência informada como "Versão V02", mas usa o mesmo arquivo `patricia_silva.png` — não há evidência de que um arquivo distinto tenha sido fornecido entre as duas datas. Portanto, esta reconciliação versiona o arquivo existente como `V01` (nome objetivo conforme o manifesto original) e mantém `PENDENTE DE IMPORTAÇÃO DA FONTE APROVADA` para a interpretação visual mais recente. Não presuma que o arquivo aqui versionado seja a "V02" aprovada até confirmação humana.

## Ingestão pendente — CHAR-003

O arquivo-fonte da nova interpretação visual de Patrícia (se distinto do V01 acima) deve ser fornecido para ingestão como `IMG-CHAR-003-PATRICIA-SILVA-MASTER-V02.<extensao-original>`. Formato, dimensões, SHA-256, origem e data de ingestão só devem ser registrados após a incorporação do arquivo real. Não existe placeholder para essa versão.
