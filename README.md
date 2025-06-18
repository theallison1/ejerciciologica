# Traducción de Lenguaje Natural a Lógica Formal

## Variables proposicionales:
- **L**: Llueve
- **C**: Hay clases
- **J**: Juan estudia
- **A**: Juan aprueba el examen
- **T**: Ana trabaja
- **P**: Pedro estudia
- **M**: María baila flamenco
- **F**: María está feliz
- **Q**: Pablo llega temprano
- **E**: Pablo puede entrar al teatro

---

## Traducciones:

1. **"Si llueve, entonces no hay clases."**  
   `L → ¬C`

2. **"Juan estudia y aprueba el examen."**  
   `J ∧ A`

3. **"No es cierto que Ana trabaje o que Pedro estudie."**  
   `¬(T ∨ P)`  
   *Equivalente (De Morgan):*  
   `¬T ∧ ¬P`

4. **"Si María baila flamenco, entonces está feliz, pero si no baila, no lo está."**  
   `(M → F) ∧ (¬M → ¬F)`  
   *Forma simplificada:*  
   `M ↔ F`

5. **"Solo si Pablo llega temprano, podrá entrar al teatro."**  
   `E → Q`  
   *(Nota: "A solo si B" ≡ `A → B`)*

---

## Resumen en tabla:

| Lenguaje Natural | Lógica Formal |
|------------------|---------------|
| Si llueve, no hay clases. | `L → ¬C` |
| Juan estudia y aprueba. | `J ∧ A` |
| No es cierto que Ana trabaje o Pedro estudie. | `¬(T ∨ P)` |
| María baila ↔ está feliz. | `M ↔ F` |
| Pablo entra al teatro solo si llega temprano. | `E → Q` |

---

### Notas:
- Usé símbolos estándar:  
  `¬` = negación, `∧` = AND, `∨` = OR, `→` = implicación, `↔` = bicondicional.





# Tablas de Verdad y Clasificación de Fórmulas Lógicas

## 1. ¬p ∨ q (Disyunción condicional)

| p | q | ¬p | ¬p ∨ q | Tipo        |
|---|---|----|--------|-------------|
| V | V | F  | V      |             |
| V | F | F  | F      | Contingencia|
| F | V | V  | V      |             |
| F | F | V  | V      |             |

**Explicación:** Esta fórmula es verdadera excepto cuando p es verdadero y q es falso.

## 2. (p → q) ∧ (q → r) (Doble implicación)

| p | q | r | p→q | q→r | Resultado | Tipo        |
|---|---|---|-----|-----|-----------|-------------|
| V | V | V | V   | V   | V         |             |
| V | V | F | V   | F   | F         | Contingencia|
| V | F | V | F   | V   | F         |             |
| V | F | F | F   | V   | F         |             |
| F | V | V | V   | V   | V         |             |
| F | V | F | V   | F   | F         |             |
| F | F | V | V   | V   | V         |             |
| F | F | F | V   | V   | V         |             |

**Explicación:** Solo es falsa cuando p→q o q→r son falsas.

## 3. (p ∨ q) ↔ (¬p → q) (Equivalencia)

| p | q | p∨q | ¬p→q | Resultado | Tipo      |
|---|---|-----|------|-----------|-----------|
| V | V | V   | V    | V         |           |
| V | F | V   | V    | V         | Tautología|
| F | V | V   | V    | V         |           |
| F | F | F   | F    | V         |           |

**Explicación:** Siempre verdadera, muestra que p∨q es equivalente a ¬p→q.

## 4. ¬(p ∧ q) → (¬p ∨ ¬q) (Ley de De Morgan)

| p | q | p∧q | ¬(p∧q) | ¬p∨¬q | Resultado | Tipo      |
|---|---|-----|--------|-------|-----------|-----------|
| V | V | V   | F      | F     | V         |           |
| V | F | F   | V      | V     | V         | Tautología|
| F | V | F   | V      | V     | V         |           |
| F | F | F   | V      | V     | V         |           |

**Explicación:** Demuestra la equivalencia entre ¬(p∧q) y ¬p∨¬q.

## 5. (p → q) ∨ (q → p) (Paradoja de la implicación)

| p | q | p→q | q→p | Resultado | Tipo      |
|---|---|-----|-----|-----------|-----------|
| V | V | V   | V   | V         |           |
| V | F | F   | V   | V         | Tautología|
| F | V | V   | F   | V         |           |
| F | F | V   | V   | V         |           |

**Explicación:** Siempre verdadera, incluso cuando p y q son contradictorias.

## Resumen de Clasificaciones

| Fórmula                  | Tipo        |
|--------------------------|-------------|
| ¬p ∨ q                   | Contingencia|
| (p → q) ∧ (q → r)        | Contingencia|
| (p ∨ q) ↔ (¬p → q)       | Tautología  |
| ¬(p ∧ q) → (¬p ∨ ¬q)     | Tautología  |
| (p → q) ∨ (q → p)        | Tautología  |

**Leyenda:**
- **Tautología**: Siempre verdadera
- **Contingencia**: Depende de los valores de verdad
- **Contradicción**: Siempre falsa (no aparece en estos ejemplos)



# Ejercicios de Simplificación Lógica

## 1. ¬(p → q) ∨ (q → r)
**Fórmula original:**  
¬(p → q) ∨ (q → r)

**Pasos de simplificación:**
1. ¬(¬p ∨ q) ∨ (¬q ∨ r)  [A → B ≡ ¬A ∨ B]
2. (p ∧ ¬q) ∨ ¬q ∨ r      [Ley de De Morgan y doble negación]
3. (p ∨ ¬q ∨ r) ∧ (¬q ∨ ¬q ∨ r) [Distributiva]
4. ¬q ∨ r                 [Absorción]

**Resultado final:**  
`¬q ∨ r`

## 2. (p ∨ q) ∧ (¬p ∨ r)
**Fórmula original:**  
(p ∨ q) ∧ (¬p ∨ r)

**Pasos de simplificación:**
1. (p ∧ ¬p) ∨ (p ∧ r) ∨ (q ∧ ¬p) ∨ (q ∧ r) [Distributiva completa]
2. F ∨ (p ∧ r) ∨ (q ∧ ¬p) ∨ (q ∧ r)        [p ∧ ¬p ≡ F]
3. (p ∧ r) ∨ (q ∧ ¬p) ∨ (q ∧ r)            [F ∨ A ≡ A]

**Resultado final:**  
`(p ∧ r) ∨ (q ∧ ¬p) ∨ (q ∧ r)`

## 3. ¬(¬p ∧ ¬q)
**Fórmula original:**  
¬(¬p ∧ ¬q)

**Pasos de simplificación:**
1. p ∨ q [Ley de De Morgan]

**Resultado final:**  
`p ∨ q`

## 4. (p → q) ∧ ¬q
**Fórmula original:**  
(p → q) ∧ ¬q

**Pasos de simplificación:**
1. (¬p ∨ q) ∧ ¬q      [A → B ≡ ¬A ∨ B]
2. (¬p ∧ ¬q) ∨ (q ∧ ¬q) [Distributiva]
3. ¬p ∧ ¬q            [q ∧ ¬q ≡ F, F ∨ A ≡ A]

**Resultado final:**  
`¬p ∧ ¬q`

## 5. (p → r) ∧ (q → r)
**Fórmula original:**  
(p → r) ∧ (q → r)

**Pasos de simplificación:**
1. (¬p ∨ r) ∧ (¬q ∨ r) [A → B ≡ ¬A ∨ B]
2. (¬p ∧ ¬q) ∨ r       [Distributiva y absorción]

**Resultado final:**  
`(¬p ∧ ¬q) ∨ r`

## Resumen de Simplificaciones

| Fórmula original         | Resultado simplificado     |
|--------------------------|----------------------------|
| ¬(p → q) ∨ (q → r)       | ¬q ∨ r                     |
| (p ∨ q) ∧ (¬p ∨ r)       | (p ∧ r) ∨ (q ∧ ¬p) ∨ (q ∧ r)|
| ¬(¬p ∧ ¬q)               | p ∨ q                      |
| (p → q) ∧ ¬q             | ¬p ∧ ¬q                    |
| (p → r) ∧ (q → r)        | (¬p ∧ ¬q) ∨ r              |

**Leyes utilizadas:**
- Ley de implicación: `A → B ≡ ¬A ∨ B`
- Ley de De Morgan: `¬(A ∧ B) ≡ ¬A ∨ ¬B`, `¬(A ∨ B) ≡ ¬A ∧ ¬B`
- Ley distributiva: `A ∨ (B ∧ C) ≡ (A ∨ B) ∧ (A ∨ C)`
- Ley de absorción: `A ∨ (A ∧ B) ≡ A`
- Complementación: `A ∧ ¬A ≡ F`, `A ∨ F ≡ A`
