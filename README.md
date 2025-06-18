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
