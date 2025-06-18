# ejerciciologica


# Traducción de Lenguaje Natural a Lógica Formal

Asignación de variables proposicionales:
- **L**: "Llueve"
- **C**: "Hay clases"
- **J**: "Juan estudia"
- **A**: "Juan aprueba el examen"
- **T**: "Ana trabaja"
- **P**: "Pedro estudia"
- **M**: "María baila flamenco"
- **F**: "María está feliz"
- **Q**: "Pablo llega temprano"
- **E**: "Pablo puede entrar al teatro"

---

## Traducciones

1. **"Si llueve, entonces no hay clases."**  
   \[
   L \to \neg C
   \]

2. **"Juan estudia y aprueba el examen."**  
   \[
   J \land A
   \]

3. **"No es cierto que Ana trabaje o que Pedro estudie."**  
   \[
   \neg (T \lor P)
   \]  
   *Equivalente por De Morgan*:  
   \[
   \neg T \land \neg P
   \]

4. **"Si María baila flamenco, entonces está feliz, pero si no baila, no lo está."**  
   \[
   (M \to F) \land (\neg M \to \neg F)
   \]  
   *Forma simplificada (bicondicional)*:  
   \[
   M \leftrightarrow F
   \]

5. **"Solo si Pablo llega temprano, podrá entrar al teatro."**  
   \[
   E \to Q
   \]  
   *Explicación*: "E solo si Q" ≡ \( E \to Q \).

---

## Resumen en Tabla

| **Lenguaje Natural** | **Lógica Formal** |
|----------------------|------------------|
| Si llueve, entonces no hay clases. | \( L \to \neg C \) |
| Juan estudia y aprueba el examen. | \( J \land A \) |
| No es cierto que Ana trabaje o que Pedro estudie. | \( \neg (T \lor P) \) |
| Si María baila flamenco, está feliz; si no baila, no lo está. | \( M \leftrightarrow F \) |
| Solo si Pablo llega temprano, podrá entrar al teatro. | \( E \to Q \) |

---

## Notas Clave
- **Implicación vs. Bicondicional**:  
  - "Si P, entonces Q" ≡ \( P \to Q \).  
  - "P si y solo si Q" ≡ \( P \leftrightarrow Q \).  
- **Negación de Disyunciones**:  
  - \( \neg (A \lor B) \) equivale a \( \neg A \land \neg B \) (Leyes de De Morgan).  
- **"Solo si"**:  
  - "A solo si B" se traduce como \( A \to B \), no como \( B \to A \).
