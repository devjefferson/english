# English Learning Log

_Append-only. Each entry starts with `## [YYYY-MM-DD]` for grep-parsability._

## [2026-04-11] setup | Wiki initialized
- Directory structure created.
- CLAUDE.md schema written for English learning.
- Ready to ingest first source.

## [2026-04-12] query | Primeira página: pronúncia de palavras do cotidiano
- Output: wiki/concepts/pronuncia-palavras-do-cotidiano.md
- Contexto: usuário nível A1, objetivo tech + cotidiano, dificuldade com pronúncia de anglicismos 
- Filed back: yes

## [2026-04-12] query | Expansão do wiki — 3 novas páginas
- Pages criadas: [[verbos-de-acao]], [[cumprimentos-e-frases-basicas]], [[frases-de-erro-e-terminal]]
- Cobertura: 46 verbos tech+cotidiano, frases prontas de trabalho, mensagens de erro/terminal/HTTP
- Filed back: yes

## [2026-09-09] aula | Simple past, verbos irregulares e pronomes
- Comando criado: .claude/commands/aula.md
- Pages criadas: [[simple-past]], [[verbos-irregulares]], [[pronomes-pessoais-e-objeto]]
- Backlinks adicionados em [[verbos-de-acao]]
- Notas: primeiras páginas de gramática da wiki. Nível A1. Drill de 12 questões proposto, aguardando respostas.

## [2026-09-09] rule | Pronúncia obrigatória
- CLAUDE.md: nova regra — toda palavra/frase em inglês leva pronúncia aproximada em PT.
- Páginas [[simple-past]], [[verbos-irregulares]], [[pronomes-pessoais-e-objeto]] reescritas com coluna/anotação de pronúncia.
- Comando .claude/commands/aula.md atualizado com o passo de pronúncia.

## [2026-09-10] output | Diálogos de prática — Simple Past
- Output: wiki/queries/dialogo-simple-past.md
- Conteúdo: 2 diálogos (fim de semana + daily meeting tech), tabela de 18 verbos, frases prontas de daily, 5 exercícios
- Backlinks adicionados em [[simple-past]] e [[verbos-irregulares]]
- Notas: exercícios aguardando respostas do usuário.

## [2026-09-16] aula | Adjetivo + substantivo e artigos a/an
- Fonte: imagem "Word It Up" (Overcome Idiomas), 10 pares adjetivo+substantivo
- Pages criadas: [[ordem-adjetivo-substantivo]], [[artigos-a-an]], [[adjetivos-descritivos-basicos]]
- Notas: nível A1. Drill de 12 questões proposto, aguardando respostas do usuário.

## [2026-09-16] refactor | Comando /aula redesenhado + retrofit de cores
- Comando `.claude/commands/aula.md` reescrito: persona "second brain" (Zettelkasten/PKM), restrições de design para memória fraca/TDAH suspeito e desmotivação (blocos curtos, vitórias frequentes, repetição espaçada), regra de escrito+pronúncia+significado, técnica das 3 cores por função gramatical (azul=sujeito, verde=verbo, amarelo=complemento).
- Retrofit aplicado às páginas com frases completas: [[simple-past]], [[verbos-irregulares]], [[pronomes-pessoais-e-objeto]], [[dialogo-simple-past]], [[verbos-de-acao]], [[ordem-adjetivo-substantivo]], [[adjetivos-descritivos-basicos]] — legenda de cores adicionada + frases-exemplo recodificadas com `<span>`.
- Páginas de listas/expressões fixas sem estrutura sujeito+verbo ([[pronuncia-palavras-do-cotidiano]], [[cumprimentos-e-frases-basicas]] parcial, [[frases-de-erro-e-terminal]], [[artigos-a-an]]) receberam nota explicando por que a técnica não se aplica integralmente, com link cruzado para o padrão completo.

## [2026-09-16] aula | Nouns: countable/uncountable, plural, números, dias e meses
- Pages criadas: [[substantivos-plural]], [[numeros]], [[dias-da-semana]], [[meses]]
- Repetição espaçada: reativados 2 itens de [[adjetivos-descritivos-basicos]] no início da aula
- Notas: nível A1. Drill de 10 questões sobre nouns proposto, aguardando respostas do usuário.

## [2026-09-16] rule | Sílaba tônica em vermelho
- Comando `.claude/commands/aula.md`: nova regra — sílaba tônica das transcrições fonéticas marcada em vermelho (`<span style="color:#ef4444">`), independente da técnica das 3 cores (sujeito/verbo/complemento).
- Retrofit aplicado às 15 páginas existentes da wiki (grammar, vocabulary, concepts, queries) via 3 agentes em paralelo.
- Notas: onde os acentos gráficos indicavam só timbre de vogal e não tonicidade real do inglês, a tônica foi ajustada por julgamento linguístico (ex: understand/understood → tônica na última sílaba).

## [2026-09-17] aula | Exceções de a/an e is/are com substantivos
- Fonte: prints da aula "Nouns and Articles" / "Nouns and Be" (Overcome Idiomas)
- Pages atualizadas: [[artigos-a-an]] (adicionadas exceções de H mudo e U com dois sons)
- Pages criadas: [[be-substantivos-is-are]] (Noun+is+Noun, negativa singular, Noun+are+Noun, negativa plural)
- Repetição espaçada: reativada a regra base de a/an (som, não letra) no início da aula
- Notas: nível A1. Drill de 10 questões proposto, aguardando respostas do usuário.

## [2026-09-17] refactor | Ampliação de [[be-substantivos-is-are]]
- Adicionados mais exemplos por seção (5 na afirmativa singular; 4 em cada negativa e plural)
- Explicações mais detalhadas: concordância it/they, motivo do artigo sumir no plural, erro comum de usar "it" com sujeito plural
