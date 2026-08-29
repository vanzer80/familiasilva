# Checklist de Episódio e Vídeo

## Antes da geração

- [ ] O prompt partiu do template mestre oficial.
- [ ] O prompt é autossuficiente e não depende de geração anterior não fornecida à ferramenta.
- [ ] Personagens, IDs, falantes e silenciosos estão listados na documentação interna.
- [ ] Cada personagem usa sua própria referência aprovada.
- [ ] **Todas** as MASTERs citadas no prompt estão realmente anexadas na geração.
- [ ] No Gemini com múltiplas referências, a ordem das MASTERs anexadas foi conferida 1:1 com a ordem dos nomes na frase de referências do prompt (regra operacional validada em `2026-08-29`; não generalizar automaticamente para outras ferramentas).
- [ ] Nenhum vídeo de Antônio ou Beto foi usado como referência facial cruzada.
- [ ] O rendering está definido como `Photorealistic / Warm Cinematic Realism`.
- [ ] Não há nome de estúdio, franquia, obra ou artista como atalho visual.
- [ ] Informações não aprovadas permanecem `A DEFINIR` e não foram inventadas.
- [ ] A duração/configuração escolhida foi verificada na ferramenta; não foi inferida apenas pela aparência da interface.

## Continuidade visual

- [ ] Rosto, idade aparente, cabelo, corpo, peso, silhueta e proporções permanecem estáveis.
- [ ] Não há morphing, mistura de personagens ou deriva facial/corporal.
- [ ] Figurino, acessórios e calçados permanecem consistentes.
- [ ] Cenário, layout, objetos, cores e iluminação permanecem consistentes.
- [ ] Não aparecem personagens, objetos, textos ou logos não solicitados.
- [ ] Mãos, dedos, membros, pele e movimentos foram revisados.
- [ ] O resultado evita cartoon, aparência infantil, pele plástica e proporções exageradas.

## Fala, voz, emoção e lip sync

- [ ] Cada fala literal pertence ao personagem correto.
- [ ] Nenhum personagem troca, completa, parafraseia ou recebe fala extra.
- [ ] Cada voz está vinculada ao personagem correto e tem status conhecido.
- [ ] Somente o falante executa o lip sync correspondente.
- [ ] Personagens silenciosos não movimentam os lábios como se falassem.
- [ ] Áudio, ritmo e inteligibilidade foram revisados.
- [ ] A fala soa como linguagem oral brasileira, não como texto excessivamente escrito.
- [ ] A direção de atuação contém a emoção específica necessária sem teatralidade exagerada.
- [ ] A fala cabe na duração **com pausas, emoção e reações**, não apenas quando lida rapidamente.
- [ ] Quando a fala ficou apertada, foram removidas palavras antes de acelerar artificialmente a interpretação ou aceitar corte de diálogo.

## Narrativa e relações

- [ ] Personalidades e limites de comportamento foram respeitados.
- [ ] Relações, nomes, apelidos e formas de tratamento estão corretos.
- [ ] Sr. Antônio não foi tratado como integrante ou parente da Família Silva.
- [ ] Humor está alinhado a [../docs/TOM-E-HUMOR.md](../docs/TOM-E-HUMOR.md).
- [ ] Nenhuma informação experimental foi apresentada como cânone.
- [ ] Se microcenas foram agrupadas, existe relação causal/emocional clara entre os beats.
- [ ] Se uma reação silenciosa entrega o payoff, não foi adicionada fala explicativa desnecessária.
- [ ] A versão curta preserva um arco compreensível mesmo quando omite subtramas da fonte histórica.

## Saída técnica

- [ ] Duração, proporção, resolução, frame rate, número de tomadas e áudio correspondem ao registro do teste.
- [ ] Cortes, transições, sincronização e artefatos foram revisados.
- [ ] A configuração usada foi registrada, inclusive quando diverge da baseline do Flow.
- [ ] Se existe arquivo de `20s`, foi distinguido o **fato do arquivo ter 20s** da interpretação sobre como a ferramenta o produziu (geração única, extensão, continuação ou sequência).
- [ ] Quando possível, o binário final foi auditado por metadata/hash em vez de depender apenas da percepção visual.

## Disciplina de validação

- [ ] Ideias e suspeitas foram marcadas como `HIPÓTESE` antes de validação.
- [ ] Um primeiro resultado positivo não foi automaticamente promovido a regra permanente.
- [ ] Comportamentos de interface/ferramenta foram reproduzidos ou objetivamente inspecionados antes de virar decisão/template.
- [ ] Fatos observados e interpretação causal estão separados no registro.

## Registro e aprovação

- [ ] O teste foi registrado em `producao/testes/`.
- [ ] Erros e soluções foram vinculados quando aplicável.
- [ ] A dimensão aprovada foi declarada sem ampliação indevida.
- [ ] Rejeições úteis foram preservadas.
- [ ] Ficha, continuidade, changelog e decisões foram atualizados quando necessário.
- [ ] O asset só foi chamado de MASTER depois de versionado e vinculado.
- [ ] Se o episódio foi publicado, plataforma, data, descrição e hashtags finais foram registradas.
