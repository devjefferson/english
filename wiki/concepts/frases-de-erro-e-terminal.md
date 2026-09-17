---
title: "Frases de erro e terminal"
type: vocabulary
level: A1
tags: [tecnologia, terminal, erros, mensagens, leitura-técnica]
created: 2026-04-12
updated: 2026-09-16
sources: []
related: [verbos-de-acao.md, pronuncia-palavras-do-cotidiano.md]
---

# Frases de erro e terminal

> Mensagens técnicas fragmentadas (sem sujeito claro, ex: `Not found`) — não usa a codificação de 3 cores. Ver legenda em [[simple-past]] para o padrão aplicado a frases completas.

Mensagens que aparecem no terminal, no navegador, no Git e em qualquer ferramenta de desenvolvimento. Entender essas frases resolve 80% dos problemas do dia a dia sem precisar de tradutor.

---

## Estrutura de uma mensagem de erro

A maioria dos erros segue um padrão:

```
[O que falhou] + [o que era esperado ou o que aconteceu]
```

Exemplos:
- *"Expected string but got number"* → Esperava texto mas recebeu número
- *"Cannot read property of undefined"* → Não consigo ler propriedade de algo indefinido
- *"Permission denied"* → Permissão negada

---

## Palavras-chave para entender erros

| Palavra            | Pronúncia        | Significado                           |
| ------------------ | ---------------- | ------------------------------------- |
| **error**          | <span style="color:#ef4444">é</span>-ror            | erro                                  |
| **warning**        | <span style="color:#ef4444">uór</span>-ning         | aviso (não bloqueia, mas é um alerta) |
| **failed**         | feild            | falhou                                |
| **success**        | sak-<span style="color:#ef4444">sés</span>          | sucesso                               |
| **expected**       | eks-<span style="color:#ef4444">pék</span>-tid      | esperado                              |
| **found**          | faund            | encontrado                            |
| **not found**      | nót faund        | não encontrado                        |
| **undefined**      | an-dih-<span style="color:#ef4444">faind</span>     | indefinido (variável sem valor)       |
| **null**           | nal              | nulo, vazio                           |
| **invalid**        | in-<span style="color:#ef4444">vé</span>-lid        | inválido                              |
| **missing**        | <span style="color:#ef4444">mí</span>-sing          | faltando, ausente                     |
| **required**       | rih-<span style="color:#ef4444">kuáird</span>       | obrigatório, necessário               |
| **denied**         | dih-<span style="color:#ef4444">naid</span>         | negado                                |
| **forbidden**      | for-<span style="color:#ef4444">bí</span>-den       | proibido (sem permissão)              |
| **timeout**        | <span style="color:#ef4444">taim</span>-aut         | tempo esgotado                        |
| **connection**     | ko-<span style="color:#ef4444">nék</span>-xon       | conexão                               |
| **refused**        | rih-<span style="color:#ef4444">fyuuzd</span>       | recusado                              |
| **already exists** | <span style="color:#ef4444">ól</span>-redi eg-<span style="color:#ef4444">zists</span> | já existe                             |
| **does not exist** | daz nót eg-<span style="color:#ef4444">zist</span>  | não existe                            |
| **cannot**         | <span style="color:#ef4444">ké</span>-not           | não consegue, não pode                |
| **unable to**      | an-<span style="color:#ef4444">éi</span>-bel tu     | incapaz de                            |
| **unexpected**     | a-nek-<span style="color:#ef4444">spék</span>-tid   | inesperado                            |
| **syntax**         | <span style="color:#ef4444">sín</span>-teks         | sintaxe (estrutura do código)         |
| **deprecated**     | <span style="color:#ef4444">dé</span>-prih-kei-tid  | obsoleto, será removido futuramente   |

---

## Mensagens de erro mais comuns

| Mensagem | O que significa |
|----------|----------------|
| `Not found` | Arquivo, rota ou recurso não existe |
| `Permission denied` | Você não tem permissão para fazer isso |
| `Connection refused` | O servidor não está aceitando conexões |
| `Connection timed out` | Demorou demais, a conexão foi encerrada |
| `File not found` | O arquivo não existe nesse caminho |
| `Command not found` | O comando digitado não existe ou não está instalado |
| `Already exists` | Você está tentando criar algo que já existe |
| `Cannot read property 'x' of undefined` | Tentou acessar algo em uma variável que não tem valor |
| `Expected X but got Y` | O código esperava um tipo/valor e recebeu outro |
| `Syntax error` | Erro na estrutura do código (vírgula faltando, parêntese errado, etc.) |
| `Deprecation warning` | Aviso de que uma função está obsoleta e será removida |
| `Module not found` | Dependência/pacote não está instalado |
| `Access denied` | Sem permissão de acesso |
| `Bad request` | A requisição enviada está errada |
| `Unauthorized` | Você precisa fazer login |
| `Forbidden` | Você está logado mas não tem permissão |
| `Internal server error` | Erro genérico no servidor |

---

## Comandos comuns no terminal

| Comando / Saída | O que significa |
|----------------|----------------|
| `git push` | Enviar alterações para o repositório |
| `git pull` | Baixar alterações do repositório |
| `npm install` | Instalar dependências |
| `npm run build` | Compilar o projeto |
| `npm start` | Iniciar o projeto |
| `yarn dev` | Rodar em modo desenvolvimento |
| `Successfully installed` | Instalado com sucesso |
| `Done in X seconds` | Concluído em X segundos |
| `Watching for changes...` | Monitorando alterações... |
| `Compiled successfully` | Compilado com sucesso |
| `Failed to compile` | Falhou ao compilar |

---

## HTTP: os códigos de status

Aparecem muito em APIs e no navegador:

| Código | Nome | Significado simples |
|--------|------|---------------------|
| **200** | OK | Funcionou |
| **201** | Created | Criado com sucesso |
| **400** | Bad Request | Você enviou algo errado |
| **401** | Unauthorized | Precisa fazer login |
| **403** | Forbidden | Não tem permissão |
| **404** | Not Found | Não encontrado |
| **500** | Internal Server Error | Erro no servidor |

---

## Conceitos relacionados

- [[Verbos de Ação]]
- [[Pronúncia: palavras do cotidiano que brasileiros falam errado]]
