# ERR-009 — Gemini: MASTERs ausentes ou fora de ordem

- **Data:** `2026-08-29`
- **Ferramenta:** Gemini, geração de vídeo
- **Status:** `ERRO OBSERVADO / CAUSA OPERACIONAL VALIDADA PELO RETESTE`
- **Episódio relacionado:** `S01E001 — A Greve da Patrícia`

## Sintoma observado

Ao gerar uma cena com múltiplos personagens, o Gemini retornou a mensagem genérica:

> `I encountered an error doing what you asked. Could you try again?`

O prompt citava vários personagens, mas nem todas as respectivas imagens MASTER haviam sido anexadas na execução.

## Causa operacional confirmada neste caso

O usuário corrigiu o envio das referências, anexando todas as MASTERs dos personagens pedidos no prompt. Depois dessa correção, a geração foi concluída com sucesso.

Portanto, **neste teste específico**, a falha não foi causada pelo conteúdo dramático da cena nem por um bloqueio explícito de política: estava associada ao conjunto incompleto de referências anexadas.

## Segunda falha relacionada — associação incorreta de personagens

O usuário também observou em testes com múltiplas referências que a ordem de anexação das MASTERs é relevante para a associação personagem ↔ referência. Quando a sequência das imagens não acompanha a sequência dos personagens no prompt, podem ocorrer:

- inversão de papéis;
- fala atribuída ao personagem errado;
- associação visual incorreta;
- geração de uma cena diferente da intenção do prompt.

Essa observação é registrada como evidência operacional do Gemini nesta rodada de produção. Não generalizar automaticamente para toda ferramenta de geração sem teste equivalente.

## Regra de prevenção

Antes de gerar uma cena com múltiplos personagens no Gemini:

1. listar os personagens na ordem em que serão citados na frase de referências do prompt;
2. anexar **todas** as MASTERs desses personagens;
3. anexar as imagens **na mesma ordem** dos nomes no prompt;
4. fazer uma checagem 1:1 antes de acionar a geração.

Exemplo:

`Use the uploaded master images of Carol, Marcos, Patrícia and Dudu...`

Ordem de anexação esperada:

1. Carol;
2. Marcos;
3. Patrícia;
4. Dudu.

## O que este erro não prova

- Não prova que todo erro genérico do Gemini tenha essa causa.
- Não prova que outras ferramentas dependam da mesma ordem de upload.
- Não autoriza remover referências para simplificar um prompt com múltiplos personagens.

## Solução vinculada

[SOL-009 — Gemini: conjunto completo e ordem das MASTERs](../solucoes/SOL-009-GEMINI-MASTERS-COMPLETAS-E-ORDENADAS.md)
