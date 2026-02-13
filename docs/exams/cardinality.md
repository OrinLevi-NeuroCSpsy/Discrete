# שאלות מבחן בנושא עוצמות

## מבחן 2024 מועד א - שאלה 2ג

### חשבון עוצמות ומשפט קנטור

**שאלה:** תהי פונקציה $G \in (\mathbb{R} \to \mathbb{R}) \to (\mathcal{P}(\mathbb{R}) \to \mathcal{P}(\mathbb{R} \times \mathbb{R}))$. הוכיחו ש-$G$ אינה על.

**רמז:** השתמשו בחשבון עוצמות.

!!! success "פתרון"
    נניח בשלילה ש-$G$ על. אז ממשפט מהכיתה:
    $$|\mathcal{P}(\mathbb{R}) \to \mathcal{P}(\mathbb{R} \times \mathbb{R})| \leq |\mathbb{R} \to \mathbb{R}|$$

    **חישוב עוצמות:**

    $$|\mathbb{R} \to \mathbb{R}| = \aleph^\aleph$$

    כאשר: $2^\aleph \leq \aleph^\aleph \leq (2^\aleph)^\aleph = 2^{\aleph \cdot \aleph} = 2^\aleph$

    מקש"ב: $|\mathbb{R} \to \mathbb{R}| = 2^\aleph$

    $$|\mathcal{P}(\mathbb{R}) \to \mathcal{P}(\mathbb{R} \times \mathbb{R})| = (2^{\aleph \cdot \aleph})^{2^\aleph} = (2^\aleph)^{2^\aleph} = 2^{\aleph \cdot 2^\aleph} = 2^{2^\aleph}$$

    קיבלנו $2^{2^\aleph} \leq 2^\aleph$, **בסתירה למשפט קנטור** ($2^a > a$).

**מושגים:** משפט קנטור, חשבון עוצמות, קש"ב

---

## מבחן 2024 מועד א - שאלה 4ג,ד

### עוצמת תמונה ומקור

**הגדרה:** $f = \lambda \langle a, b \rangle \in \mathbb{N}_{even} \times \mathbb{N}_{odd}. \frac{a}{b}$

**סעיף ג:** מצאו את עוצמת $\text{Im}(f)$.

!!! success "פתרון: $\aleph_0$"
    **חסם עליון:** $\text{Im}(f) \subseteq \mathbb{Q}$, לכן $|\text{Im}(f)| \leq |\mathbb{Q}| = \aleph_0$

    **חסם תחתון:** לכל $n \in \mathbb{N}_{even}$: $n = f(\langle n, 1 \rangle) \in \text{Im}(f)$

    לכן $\mathbb{N}_{even} \subseteq \text{Im}(f)$ ומכאן $|\text{Im}(f)| \geq \aleph_0$

**סעיף ד:** מצאו את עוצמת $A = f^{-1}[\{2/3\}]$.

!!! success "פתרון: $\aleph_0$"
    **חסם עליון:** $A \subseteq \mathbb{N}_{even} \times \mathbb{N}_{odd}$, לכן $|A| \leq \aleph_0$

    **חסם תחתון:** נגדיר $h = \lambda n \in \mathbb{N}. \langle 2 \cdot 5^n, 3 \cdot 5^n \rangle$

    - $h$ לטווח הנכון: $f(h(n)) = \frac{2 \cdot 5^n}{3 \cdot 5^n} = \frac{2}{3}$
    - $h$ חח"ע: אם $h(n_1) = h(n_2)$ אז $2 \cdot 5^{n_1} = 2 \cdot 5^{n_2}$, לכן $n_1 = n_2$

    מכאן $|A| \geq \aleph_0$

---

## מבחן 2023 מועד א - שאלה 4

### לכסון - קבוצה לא בת מנייה

**שאלה:** נסמן $X = \{B \in \mathcal{P}(\mathbb{N}) \mid |B| = \aleph_0 \land |\mathbb{N} \setminus B| = \aleph_0\}$

הוכיחו ש-$X$ אינה בת מנייה.

!!! success "פתרון בלכסון"
    נניח בשלילה שקיים זיווג $F: \mathbb{N} \to X$.

    נגדיר:
    $$B = \{n \in \mathbb{N} \mid \exists k. n = 3k \land n \notin F(k)\} \cup \{n \in \mathbb{N} \mid \exists k. n = 3k + 1\}$$

    **$B \in X$:**

    - $\{3k+1 \mid k \in \mathbb{N}\} \subseteq B$ - קבוצה אינסופית, לכן $B$ אינסופית
    - $\{3k+2 \mid k \in \mathbb{N}\} \subseteq \mathbb{N} \setminus B$ - לכן $\mathbb{N} \setminus B$ אינסופית

    **סתירה:** קיים $k$ עם $F(k) = B$. נסמן $n = 3k$:

    $$n \in B \iff n \notin F(k) = B$$

    **סתירה!** לכן $X$ אינה בת מנייה.

---

## מבחן 2025 מועד א - שאלה 4א

### זיווג $\mathcal{P}^* \sim \mathcal{P}(\mathbb{N})$

**הגדרה:** $\mathcal{P}^* = \{X \in \mathcal{P}(\mathbb{N}) \mid |X| \geq 2\}$

**שאלה:** הראו זיווג ע"י פונקציה מפורשת.

!!! success "פתרון"
    נגדיר $G \in \mathcal{P}(\mathbb{N}) \to \mathcal{P}^*$:

    $$G(X) = \begin{cases}
    \{0, 1\} & X = \emptyset \\
    \{x + 2 \mid x \in X\} \cup \{0\} & |X| = 1 \\
    \{x + 1 \mid x \in X\} & |X| = 2 \\
    X & \text{אחרת}
    \end{cases}$$

    **$G$ חח"ע:** לפי עוצמת $G(X)$:

    - $|G(X)| > 2$: $X = G(X)$, לכן $X_1 = X_2$
    - $|G(X)| = 2$:
        - $G(X) = \{0,1\}$: $X = \emptyset$
        - $0 \in G(X)$: $X = \{y-2 \mid y \in G(X) \setminus \{0\}\}$
        - אחרת: $X = \{x-1 \mid x \in G(X)\}$

---

## מבחן 2025 מועד א - שאלה 4ב

### עוצמת קבוצה $C$

**הגדרה:** $C = \{f \in \mathcal{P}^* \to \mathbb{N} \mid \forall X \in \mathcal{P}^*. f(X) \in X\}$

**שאלה:** מצאו את עוצמת $C$.

!!! success "פתרון: $2^\aleph$"
    **חסם עליון:**
    $$|C| \leq |\mathcal{P}^* \to \mathbb{N}| = \aleph_0^{|\mathcal{P}^*|} = \aleph_0^\aleph \leq 2^\aleph$$

    **חסם תחתון:** נגדיר $F \in \mathcal{P}(\mathcal{P}^*) \to C$:

    $$F(Y)(X) = \begin{cases}
    \min(X) & X \in Y \\
    \min(X \setminus \{\min(X)\}) & X \notin Y
    \end{cases}$$

    $F$ חח"ע: $X \in Y_1 \iff F(Y_1)(X) = \min(X) \iff F(Y_2)(X) = \min(X) \iff X \in Y_2$

    לכן $|C| \geq |\mathcal{P}(\mathcal{P}^*)| = 2^\aleph$

    **מקש"ב:** $|C| = 2^\aleph$

---

## מבחן 2025 מועד א - שאלה 5ג

### לכסון - אינה מעוצמת הרצף

**שאלה:** הוכיחו בלכסון ש-$A = \{f \in \mathcal{P}(\mathbb{N}) \to \mathcal{P}(\mathbb{N}) \mid |f^{-1}[\{\mathbb{N}_{even}\}]| = \aleph\}$ אינה מעוצמת הרצף.

!!! success "פתרון"
    נניח בשלילה שיש זיווג $F \in \mathcal{P}(\mathbb{N}^+) \to A$.

    נגדיר:
    $$f(X) = \begin{cases}
    \mathbb{N}_{even} & 0 \in X \\
    F(X)(X) \triangle \{0\} & 0 \notin X
    \end{cases}$$

    **$f \in A$:** $f^{-1}[\{\mathbb{N}_{even}\}] \supseteq \{X \mid 0 \in X\}$, ועוצמתה $\aleph$.

    **סתירה:** קיים $X \in \mathcal{P}(\mathbb{N}^+)$ עם $F(X) = f$ ו-$0 \notin X$:

    $$F(X)(X) = f(X) = F(X)(X) \triangle \{0\}$$

    מכאן $\{0\} = \emptyset$ - **סתירה!**

---

## טבלת סיכום

| מושג | שאלות |
|------|-------|
| **משפט קנטור** | 2024-2ג, 2025-4ב |
| **לכסון** | 2023-4, 2025-5ג |
| **קש"ב** | 2024-4ג,ד, 2025-4ב |
| **חשבון עוצמות** | 2024-2ג, 2025-4ב, 2025-5א |
| **זיווגים** | 2025-4א |

---

## טיפים

!!! tip "טיפים לשאלות עוצמות"
    1. **קש"ב:** הראו חסם עליון + חסם תחתון
    2. **לכסון:** בנו איבר ש"שונה באלכסון" מכל איבר בתמונה
    3. **חשבון עוצמות:** זכרו $\aleph^\aleph = 2^\aleph$, $\aleph \cdot \aleph = \aleph$
    4. **משפט קנטור:** $2^a > a$ לכל עוצמה
