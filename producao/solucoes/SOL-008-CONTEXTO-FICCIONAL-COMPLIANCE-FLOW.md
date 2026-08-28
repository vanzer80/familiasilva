# SOL-008 — Contexto ficcional/compliance simplificado para bloqueio "pessoa famosa" no Flow

- **Erro relacionado:** [ERR-008](../erros/ERR-008-FLOW-FALSO-POSITIVO-PESSOA-FAMOSA.md).
- **Quando aplicar:** **apenas** quando uma geração for efetivamente bloqueada por suspeita de retratar pessoa real/famosa. Não é um requisito universal — para gerações sem esse bloqueio, continua valendo o template enxuto padrão de [TEMPLATE-MESTRE-VIDEO.md](../../prompts/templates/TEMPLATE-MESTRE-VIDEO.md), incluindo o wording padrão de referência MASTER já documentado ali.

## Procedimento validado

1. Deixar explícito que o personagem é ficcional original: `"This scene features an original fictional character created exclusively for the fictional Brazilian family comedy Família Silva."`
2. Descrever a imagem anexada como referência pertencente ao projeto, sem intenção de retratar pessoa real: `"The attached project-owned reference image represents this fictional character and is not intended to depict or imitate any real person or public figure."`
3. Simplificar a referência visual: `"A reference image is attached for the character; match the established appearance consistently."`
4. Manter, sem enfraquecer, o requisito de rendering: `"Create a live-action photorealistic scene with real human beings, natural skin texture, realistic hair and clothing, believable human anatomy and warm cinematic lighting, filmed like real professional camera footage inside a real Brazilian environment."`
5. Evitar, especialmente nesses casos de bloqueio: `"EXACTLY the same person"`, `"absolute source of truth for identity"`, `"biometric identity"`, `"face cloning"`, linguagem extensa de likeness/identidade, e longas listas de negative constraints.

## Resultado

Após a reformulação, as três gerações (Dudu, Sr. Antônio, Beto) funcionaram no Flow. **Fato:** o bloqueio desapareceu após a reformulação do prompt. **Não comprovado:** qual elemento específico da reformulação foi decisivo, e se a causa original era realmente relacionada à aparência dos personagens — permanece hipótese, não fato (ver [ERR-008](../erros/ERR-008-FLOW-FALSO-POSITIVO-PESSOA-FAMOSA.md)).

## Estado

`VALIDADO COMO FALLBACK` — aplicável quando ocorrer o bloqueio específico de pessoa famosa; não é regra obrigatória para prompts que não apresentem esse bloqueio.
