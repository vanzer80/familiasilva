# ERR-004 — Prompt dependente de contexto anterior

- **Sintoma:** instrução como “igual ao vídeo aprovado” sem repetir os atributos nem fornecer a referência na geração atual.
- **Causa:** o Flow/Veo não recebe automaticamente materiais de uma geração anterior.
- **Impacto:** o modelo preenche lacunas livremente e produz deriva.
- **Solução:** [SOL-004](../solucoes/SOL-004-PROMPT-AUTOSSUFICIENTE.md).
- **Estado:** `SOLUÇÃO ADOTADA`.
