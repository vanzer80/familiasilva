# SOL-009 — Gemini: conjunto completo e ordem das MASTERs

- **Data:** `2026-08-29`
- **Ferramenta:** Gemini, geração de vídeo
- **Status:** `SOLUÇÃO VALIDADA NESTA RODADA`
- **Erro vinculado:** [ERR-009](../erros/ERR-009-GEMINI-MASTERS-AUSENTES-OU-FORA-DE-ORDEM.md)

## Solução

Em cenas com múltiplos personagens no Gemini, usar um conjunto completo de referências e manter alinhamento explícito entre a ordem dos nomes no prompt e a ordem das imagens anexadas.

### Procedimento

1. definir a frase de referência do prompt;
2. extrair dela a sequência dos personagens;
3. anexar a MASTER V02 PHOTOREALISTIC de cada personagem, sem omissões;
4. manter a mesma ordem do texto;
5. conferir o pareamento 1:1 antes de gerar.

Exemplo:

```text
Use the uploaded master images of Carol, Marcos, Patrícia and Dudu as visual references and preserve their established appearance consistently.
```

Anexar nesta ordem:

1. Carol;
2. Marcos;
3. Patrícia;
4. Dudu.

## Resultado do reteste

Após o usuário anexar todas as referências necessárias e corrigir a sequência, a geração que havia falhado foi concluída corretamente.

## Aplicação

- Esta solução deve ser tratada como regra operacional específica de geração com múltiplas referências no Gemini enquanto continuar reproduzível.
- O princípio mais geral — cada personagem usar sua própria MASTER — já é canônico e continua válido em qualquer ferramenta.
- Não assumir automaticamente que outras ferramentas exigem a mesma ordem de upload sem validação equivalente.
