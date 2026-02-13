# שאלות מבחן בנושא פונקציות

## מבחן 2025 מועד א - שאלה 2

### הגדרות

עבור פונקציה $f \in \mathbb{N} \to \mathbb{N}^+$ ו-$i \in \mathbb{N}^+$ נגדיר את $f^{(i)} \in \mathbb{N} \to \mathbb{N}^+$, ההרכבה של $f$ עם עצמה $i$ פעמים:

$$f^{(1)} = f$$
$$\forall i \in \mathbb{N}^+. f^{(i+1)} = f^{(i)} \circ f$$

נגדיר פונקציה $F \in (\mathbb{N} \to \mathbb{N}^+) \to \mathcal{P}(\mathbb{N}^+)$ על ידי:
$$F = \lambda f \in (\mathbb{N} \to \mathbb{N}^+). \bigcup_{i \in \mathbb{N}^+} \{f^{(i)}(0)\}$$

---

### סעיף א - פונקציות שונות עם אותה תמונה (5 נק')

**שאלה:** תנו דוגמא לפונקציות $f_1, f_2 \in \mathbb{N} \to \mathbb{N}^+$ כך ש-$F(f_1) = F(f_2)$ אבל $f_1 \neq f_2$. כתבו למה שווה $F(f_1)$.

!!! success "פתרון"
    $$f_1 = \lambda n \in \mathbb{N}. 1$$

    $$f_2 = \lambda n \in \mathbb{N}. \begin{cases} 1 & n \leq 1 \\ 2 & n > 1 \end{cases}$$

    $$F(f_1) = \{1\}$$

**מושגים נבחנים:** כתיב למבדא, הרכבת פונקציות, תמונה של פונקציה

---

### סעיף ב - חח"ע גוררת תמונה אינסופית (7 נק')

**שאלה:** הוכיחו שאם פונקציה $f \in \mathbb{N} \to \mathbb{N}^+$ היא חח"ע אז $F(f)$ אינה סופית.

!!! success "פתרון"
    נגדיר פונקציה $g \in \mathbb{N}^+ \to F(f)$ ע"י $g = \lambda n \in \mathbb{N}^+. f^{(n)}(0)$.

    **$g$ לטווח הנכון:** לכל $n \in \mathbb{N}^+$, $g(n) = f^{(n)}(0) \in \bigcup_{i \in \mathbb{N}^+} \{f^{(i)}(0)\} = F(f)$.

    **$g$ חח"ע:** יהיו $n, m \in \mathbb{N}^+$ כך ש-$g(n) = g(m)$, כלומר $f^{(n)}(0) = f^{(m)}(0)$.

    נניח בשלילה $n \neq m$. בה"כ $n > m$.

    מתקיים: $f^{(n)}(0) = (f^{(m)} \circ f^{(n-m)})(0) = f^{(m)}(f^{(n-m)}(0))$.

    הרכבה של פונקציות חח"ע היא חח"ע, לכן $f^{(m)}$ חח"ע.

    קיבלנו: $f^{(m)}(f^{(n-m)}(0)) = f^{(n)}(0) = f^{(m)}(0)$

    מחח"ע של $f^{(m)}$: $f^{(n-m)}(0) = 0$, אבל $0 \notin \mathbb{N}^+$ וזה הטווח של $f^{(n-m)}$ - **סתירה!**

    לכן $g$ חח"ע, ומכאן $|F(f)| \geq |\mathbb{N}^+| = \aleph_0$, כלומר $F(f)$ אינסופית.

---

### סעיף ג - כל קבוצה בת-מניה בתמונה (8 נק')

**שאלה:** הוכיחו שלכל $A \in \mathcal{P}(\mathbb{N}^+)$ כך ש-$|A| = \aleph_0$ מתקיים $A \in \text{Im}(F)$.

!!! success "פתרון"
    בהינתן קבוצה $A$ בת-מניה, נגדיר:
    $$f = \lambda n \in \mathbb{N}. \min\{a \in A \mid a > n\}$$

    **$f$ מוגדרת היטב:** $A$ אינסופית, לכן לכל $n$ יש איבר ב-$A$ גדול מ-$n$.

    **נוכיח $F(f) = A$:**

    - $F(f) \subseteq A$: מהגדרת $f$, כל ערך שהיא מחזירה הוא ב-$A$.

    - $A \subseteq F(f)$: יהי $b \in A$. אם $b = \min(A)$ אז $f(0) = b$. אחרת, יש $c < b$ ב-$A$. יהי $c$ המקסימלי ב-$A$ הקטן מ-$b$. קיים $n$ כך ש-$f^{(n)}(0) = c$. אז:
    $$f^{(n+1)}(0) = f(c) = \min\{a \in A \mid a > c\} = b$$

---

## מבחן 2025 מועד א - שאלה 3

### הגדרה

תהי $A$ קבוצה לא ריקה. נגדיר:
$$H = \lambda B \in \mathcal{P}(\mathcal{P}(A)). \bigcup_{C \in B} \bigcup_{a \in C} \{a\} \times C$$

---

### סעיף א - חישוב מפורש (3 נק')

**שאלה:** עבור $A = \mathbb{N}$, ו-$B = \{\mathbb{N}_{even}, \mathbb{N}_{odd}\}$, תנו ביטוי מפורש ל-$H(B)$.

!!! success "פתרון"
    $$H(B) = \mathbb{N}_{even}^2 \cup \mathbb{N}_{odd}^2$$

---

### סעיף ב - חלוקה גוררת יחס שקילות (7 נק')

**שאלה:** הוכיחו או הפריכו: אם $B$ חלוקה של $A$ אז $H(B)$ יחס שקילות על $A$.

!!! success "פתרון - הטענה נכונה"
    נשים לב שמתקיים:
    $$H(B) = \{\langle x, y \rangle \in A \times A \mid \exists C \in B. x \in C \land y \in C\}$$

    **רפלקסיביות:** יהי $a \in A$. מ-$B$ חלוקה, קיימת $C \in B$ כך ש-$a \in C$, לכן $\langle a, a \rangle \in C \times C \subseteq H(B)$.

    **סימטריות:** אם $\langle a, b \rangle \in H(B)$ אז קיימת $C \in B$ עם $a, b \in C$, לכן גם $\langle b, a \rangle \in C \times C \subseteq H(B)$.

    **טרנזיטיביות:** יהיו $\langle a, b \rangle, \langle b, c \rangle \in H(B)$. קיימות $C_1, C_2 \in B$ עם $a, b \in C_1$ ו-$b, c \in C_2$. כיוון ש-$b \in C_1 \cap C_2$ ו-$B$ חלוקה (קבוצות זרות), $C_1 = C_2$. לכן $a, c \in C_1$ ו-$\langle a, c \rangle \in H(B)$.

---

### סעיף ג - יחס שקילות לא גורר חלוקה (7 נק')

**שאלה:** הוכיחו או הפריכו: אם $H(B)$ יחס שקילות על $A$ אז $B$ חלוקה של $A$.

!!! danger "פתרון - הטענה לא נכונה"
    **דוגמה נגדית:**
    $$A = \{1, 2\}$$
    $$B = \{\{1\}, \{1, 2\}\}$$

    $H(B) = A \times A$ הוא היחס המלא - יחס שקילות.

    אבל $B$ **אינה חלוקה** כי $\{1\} \cap \{1,2\} = \{1\} \neq \emptyset$.

---

## מבחן 2023 מועד א - שאלה 3

### הגדרה

בהינתן $A, B$ קבוצות, נגדיר:
$$G = \lambda S \in \mathcal{P}(A \times B). \lambda X \in \mathcal{P}(A). \bigcup_{a \in X} \{b \in B \mid \langle a, b \rangle \in S\}$$

---

### סעיף א - הוכחת חח"ע (8 נק')

**שאלה:** הוכיחו או הפריכו: אם $A, B$ לא ריקות, $G$ חח"ע.

!!! success "פתרון - הטענה נכונה"
    יהיו $S_1 \neq S_2 \in \mathcal{P}(A \times B)$. בה"כ קיים $\langle x, y \rangle \in S_1 \setminus S_2$.

    נראה ש-$G(S_1) \neq G(S_2)$:

    - $y \in G(S_1)(\{x\})$ כי $\langle x, y \rangle \in S_1$
    - $y \notin G(S_2)(\{x\})$ כי $\langle x, y \rangle \notin S_2$

    לכן $G(S_1) \neq G(S_2)$, ו-$G$ חח"ע.

---

### סעיף ב - הפרכת על (9 נק')

**שאלה:** הוכיחו או הפריכו: אם $A, B$ לא ריקות, $G$ על $\mathcal{P}(A) \to \mathcal{P}(B)$.

!!! danger "פתרון - הטענה לא נכונה"
    מהגדרת $G$, לכל $S \in \mathcal{P}(A \times B)$ מתקיים $G(S)(\emptyset) = \emptyset$.

    נגדיר $f = \lambda X \in \mathcal{P}(A). B$.

    מתקיים $f(\emptyset) = B \neq \emptyset$ (כי $B$ לא ריקה).

    לכן לא קיים $S$ עבורו $G(S) = f$, ו-$G$ **לא על**.

---

## סיכום מושגי מפתח

| מושג | תיאור |
|------|-------|
| **חח"ע** | $f(x) = f(y) \Rightarrow x = y$ |
| **על** | $\forall b \in B. \exists a \in A. f(a) = b$ |
| **הרכבת פונקציות** | $(f \circ g)(x) = f(g(x))$ |
| **כתיב למבדא** | $f = \lambda x \in A. \text{expression}$ |
| **תמונה** | $\text{Im}(f) = \{f(x) \mid x \in \text{Dom}(f)\}$ |
| **זיווג** | פונקציה חח"ע ועל |

---

## טיפים לשאלות פונקציות

!!! tip "טיפים"
    1. **הוכחת חח"ע:** הניחו $f(x_1) = f(x_2)$ והראו $x_1 = x_2$
    2. **הוכחת על:** לכל $y$ בטווח, מצאו $x$ בתחום עם $f(x) = y$
    3. **הפרכה:** מספיקה דוגמה נגדית אחת!
    4. **כתיב למבדא:** שימו לב למשתנים קשורים וחופשיים
    5. **הרכבות:** $(f \circ g)(x) = f(g(x))$ - קודם $g$, אח"כ $f$
