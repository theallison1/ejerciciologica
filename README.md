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
- Las fórmulas están en formato de código (`texto entre backticks`) para mejor legibilidad.





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
