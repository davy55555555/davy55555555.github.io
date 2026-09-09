# 📌 Checklist da Aula 1 — Respostas

Verificação de compreensão dos conceitos fundamentais de Linguagens Formais.

---

## 1. O que é um alfabeto Σ?

**Resposta:** Um alfabeto Σ é um conjunto finito de símbolos. Exemplo: Σ = {a, b, 0, 1}.

---

## 2. O que é uma cadeia?

**Resposta:** Uma cadeia (ou palavra) é uma sequência finita de símbolos do alfabeto. Exemplo: "abba" é uma cadeia sobre Σ = {a, b}.

---

## 3. O que significa ε?

**Resposta:** ε representa a cadeia vazia — a palavra que não contém nenhum símbolo.

---

## 4. Por que |ε| = 0?

**Resposta:** |w| denota o comprimento (número de símbolos) da cadeia w. Como ε não contém símbolo algum, seu comprimento é 0.

---

## 5. O que é um prefixo?

**Resposta:** Um prefixo de uma cadeia w é qualquer sequência de símbolos que aparece no início de w. 

**Exemplo:** Para w = "abc", os prefixos são: ε, "a", "ab", "abc".

---

## 6. O que é um sufixo?

**Resposta:** Um sufixo de uma cadeia w é qualquer sequência de símbolos que aparece no final de w.

**Exemplo:** Para w = "abc", os sufixos são: ε, "c", "bc", "abc".

---

## 7. O que significa Σ*?

**Resposta:** Σ* é o conjunto de **todas** as cadeias finitas (incluindo ε) construídas a partir dos símbolos de Σ.

**Exemplo:** Se Σ = {a, b}, então Σ* = {ε, a, b, aa, ab, ba, bb, aaa, ...}.

---

## 8. Se Σ* possui limite de tamanho?

**Resposta:** Em geral, Σ* é **infinito** se Σ contém pelo menos um símbolo (pois há cadeias de todos os comprimentos: 0, 1, 2, 3, ...). 

Se Σ é vazio (Σ = ∅), então Σ* = {ε} e tem tamanho 1.

---

## 9. O que é uma linguagem formal L?

**Resposta:** Uma linguagem formal L é um conjunto (possivelmente infinito) de cadeias sobre um alfabeto Σ. Formalmente: L ⊆ Σ*.

**Exemplo:** L = {aⁿ | n ≥ 0} = {ε, a, aa, aaa, ...} é uma linguagem sobre Σ = {a}.

---

## 10. O que significa L ⊆ Σ*?

**Resposta:** Significa que **toda cadeia em L é formada por símbolos de Σ**; ou seja, L é um subconjunto do conjunto de todas as cadeias sobre Σ. Nenhuma cadeia em L contém símbolos fora de Σ.

---

## 11. O que é uma gramática formal?

**Resposta:** Uma gramática formal é uma quádrupla G = (N, Σ, P, S) onde:
- **N** é o conjunto de não-terminais (variáveis)
- **Σ** é o conjunto de terminais (alfabeto)
- **P** é o conjunto de regras de produção
- **S** é o símbolo inicial (S ∈ N)

---

## 12. O que são terminais e não-terminais?

**Resposta:** 
- **Terminais** são os símbolos que aparecem nas cadeias finais (símbolos "reais" do alfabeto).
- **Não-terminais** (ou variáveis) são símbolos usados durante a derivação para gerar cadeias; são substituídos por outras cadeias por meio das regras.

**Exemplo:** Em G = ({S}, {a}, {S → aS | ε}, S):
  - Terminais: {a}
  - Não-terminais: {S}

---

## 13. O que é uma regra de produção?

**Resposta:** É uma regra do tipo **A → α**, onde:
- **A** é um não-terminal
- **α** é uma cadeia de terminais e/ou não-terminais

A regra indica como substituir A durante a derivação.

**Exemplo:** S → aS significa "S pode ser substituído por aS".

---

## 14. Como ler S → aS | ε?

**Resposta:** "S produz aS **ou** ε" — a regra significa que a partir de S você pode substituir por "aS" **ou** pela cadeia vazia "ε".

Esta é uma forma abreviada de escrever duas regras:
- S → aS
- S → ε

---

## 15. Como gerar palavras usando uma gramática?

**Resposta:** O processo é chamado **derivação**:

1. Começa-se pelo símbolo inicial **S**
2. Aplica-se regras de produção repetidamente
3. Substitui-se não-terminais até obter uma cadeia composta **apenas por terminais**

**Exemplo com G = ({S}, {a}, {S → aS | ε}, S):**

| Derivação | Resultado |
|-----------|----------|
| S ⇒ ε | Gera a palavra vazia |
| S ⇒ aS ⇒ aε = a | Gera "a" |
| S ⇒ aS ⇒ aaS ⇒ aaε = aa | Gera "aa" |
| S ⇒ aS ⇒ aaS ⇒ aaaS ⇒ aaaε = aaa | Gera "aaa" |

Generalizando: **L(G) = {aⁿ | n ≥ 0}** (qualquer quantidade de a's, incluindo zero).

---

## 📋 Resumo de Domínio

Se você conseguiu responder todas as 15 perguntas e compreendeu os exemplos, você está pronto para:

✅ Entender a Hierarquia de Chomsky  
✅ Trabalhar com autômatos finitos  
✅ Analisar linguagens formais  
✅ Avançar para a Aula 2 (Gramáticas e Chomsky)
