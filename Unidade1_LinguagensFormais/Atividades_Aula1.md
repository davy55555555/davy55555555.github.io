# Aula 1 — Atividades Práticas (respostas)

Referência: `Notas_de_Aula.md`, seção 12 (Atividades Práticas).

## Atividade 1 — Prefixos e Sufixos

Considere a palavra:

```text
ab
```

### Prefixos

Um prefixo é uma parte da palavra que começa no início:

```text
Prefixos(ab) = {ε, a, ab}
```

### Sufixos

Um sufixo é uma parte da palavra que termina no final:

```text
Sufixos(ab) = {ε, b, ab}
```

### Observação

A palavra vazia `ε` é, ao mesmo tempo, prefixo e sufixo de qualquer palavra,
pois `|ε| = 0` e ela pode ser vista tanto no início quanto no fim de `ab`
sem contradizer nenhuma das duas definições.

---

## Atividade 2 — Gramática

Considere a gramática:

```text
G = ({S}, {a}, {S → aS | ε}, S)
```

Onde:

| Elemento | Valor |
|---|---|
| Não terminais (`N`) | `{S}` |
| Terminais (`Σ`) | `{a}` |
| Produções (`P`) | `S → aS \| ε` |
| Símbolo inicial (`S`) | `S` |

### Três palavras geradas, com derivação

**1. `ε`**

```text
S → ε
```

**2. `a`**

```text
S → aS → aε → a
```

**3. `aa`**

```text
S → aS → aaS → aaε → aa
```

### Generalização

Essa gramática gera exatamente a linguagem:

```text
L(G) = {aⁿ | n ≥ 0}
```

ou seja, qualquer quantidade (incluindo zero) do símbolo `a`.
