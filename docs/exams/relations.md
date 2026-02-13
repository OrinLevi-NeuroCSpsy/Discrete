# שאלות מבחן בנושא יחסים

## מבחן 2024 מועד ב - שאלה 1

### יחסים שלישוניים והרכבות

**הגדרה:** יחס $S$ על קבוצה $A$ נקרא **שלישוני** אם:
$$\forall a, b, c. \langle a, b \rangle \in S \land \langle b, c \rangle \in S \rightarrow \langle c, a \rangle \in S$$

**הגדרה:** הרכבה של יחס עם עצמו:
$$S^{(0)} = I_A, \quad \forall n \in \mathbb{N}. S^{(n+1)} = S^{(n)} \circ S$$

---

### סעיף א - יחס שקילות הוא שלישוני (5 נק')

**שאלה:** הוכיחו: אם $S$ יחס שקילות על $A$, אז $S$ שלישוני.

!!! success "פתרון"
    יהי $S$ יחס שקילות על $A$. יהיו $a, b, c$ שרירותיים עם $\langle a, b \rangle \in S$ ו-$\langle b, c \rangle \in S$.

    - מטרנזיטיביות של $S$: $\langle a, c \rangle \in S$
    - מסימטריה של $S$: $\langle c, a \rangle \in S$ ✓

---

### סעיף ב - יחס מלא ושלישוני (7 נק')

**שאלה:** הוכיחו: אם $S$ מלא על $A$ ושלישוני, אז $S^{(3)}$ רפלקסיבי על $A$.

!!! success "פתרון"
    יהי $S$ מלא ושלישוני על $A$. יהי $a \in A$.

    מ-$S$ מלא, קיים $b \in A$ כך ש-$\langle a, b \rangle \in S$.

    באופן דומה, קיים $c \in A$ כך ש-$\langle b, c \rangle \in S$.

    מ-$S$ שלישוני: $\langle c, a \rangle \in S$

    מהגדרת הרכבה: $\langle a, c \rangle \in S \circ S = S^{(2)}$

    לכן: $\langle a, a \rangle \in S^{(2)} \circ S = S^{(3)}$ ✓

---

### סעיף ג - איחוד הרכבות רפלקסיבי (8 נק')

**שאלה:** הוכיחו: אם $S$ מלא על $A$ וקיים $k \in \mathbb{N}^+$ כך ש-$S^{(k)}$ שלישוני, אז $\bigcup_{n \in \mathbb{N}^+} S^{(n)}$ רפלקסיבי על $A$.

!!! success "פתרון"
    יהי $a \in A$ ונסמן $T = S^{(k)}$.

    מאחר שהרכבה משמרת מלאות, $T$ מלא ושלישוני.

    לפי סעיף ב, $T^{(3)}$ רפלקסיבי.

    שימו לב: $T^{(3)} = S^{(3k)}$, שזו תת-קבוצה של $\bigcup_{n \in \mathbb{N}^+} S^{(n)}$.

    לכן: $\langle a, a \rangle \in S^{(3k)} \subseteq \bigcup_{n \in \mathbb{N}^+} S^{(n)}$ ✓

---

## מבחן 2024 מועד ב' - שאלה 2

### הרכבת יחסים ותכונות פונקציות

**שאלה:** הוכיחו או הפריכו: לכל קבוצות $A, B, C$ ויחסים $T \subseteq A \times B$, $S \subseteq B \times C$:

---

### סעיף א - הרכבה פונקציה גוררת מלאות (6 נק')

**טענה:** אם $S \circ T$ פונקציה מ-$A$ ל-$C$, אז $T$ מלא על $A$.

!!! success "פתרון - הטענה נכונה"
    יהי $a \in A$. מאחר ש-$S \circ T$ פונקציה, היא מלאה על $A$.

    לכן קיים $c \in C$ כך ש-$\langle a, c \rangle \in S \circ T$.

    מהגדרת הרכבה, קיים $b \in B$ כך ש-$\langle a, b \rangle \in T$ ו-$\langle b, c \rangle \in S$.

    לכן $T$ מלא על $A$ ✓

---

### סעיף ב - הרכבה פונקציה וחד-ערכיות (6 נק')

**טענה:** אם $S \circ T$ פונקציה מ-$A$ ל-$C$, אז $S$ חד-ערכי.

!!! danger "פתרון - הטענה לא נכונה"
    **דוגמה נגדית:**

    - $A = \{1, 2\}$, $B = \{3, 4\}$, $C = \{5, 6\}$
    - $T = \{\langle 1, 3 \rangle, \langle 2, 3 \rangle\}$
    - $S = \{\langle 3, 5 \rangle, \langle 4, 5 \rangle, \langle 4, 6 \rangle\}$

    אז $S \circ T = \{\langle 1, 5 \rangle, \langle 2, 5 \rangle\}$ - פונקציה!

    אבל $S$ לא חד-ערכי כי $\langle 4, 5 \rangle$ ו-$\langle 4, 6 \rangle$ שניהם ב-$S$.

---

### סעיף ג - $T$ לא חד-ערכי גורר $S$ לא חח"ע (8 נק')

**טענה:** אם $S \circ T$ פונקציה מ-$A$ ל-$C$, $S$ פונקציה מ-$B$ ל-$C$, ו-$T$ לא חד-ערכי, אז $S$ לא חח"ע.

!!! success "פתרון - הטענה נכונה"
    מ-$T$ לא חד-ערכי, קיימים $a \in A$, $b_1 \neq b_2 \in B$ כך ש-$\langle a, b_1 \rangle, \langle a, b_2 \rangle \in T$.

    מאחר ש-$S$ פונקציה, נסמן $c_1 = S(b_1)$, $c_2 = S(b_2)$.

    אז $\langle a, c_1 \rangle, \langle a, c_2 \rangle \in S \circ T$.

    מאחר ש-$S \circ T$ פונקציה (חד-ערכית), $c_1 = c_2$.

    קיבלנו $S(b_1) = S(b_2)$ עם $b_1 \neq b_2$.

    לכן $S$ לא חח"ע ✓

---

## מבחן 2025 מועד א - שאלה 1

### יחסים על קבוצת החזקה

**הגדרה:** יהי יחס $S_{A,B}$ מ-$A$ ל-$\mathcal{P}(B)$:
$$S_{A,B} = \{\langle a, X \rangle \in A \times \mathcal{P}(B) \mid a \notin X\}$$

---

### סעיף א - יחס מלא (5 נק')

**שאלה:** הוכיחו או הפריכו: לכל שתי קבוצות $A, B$, היחס $S_{A,B}$ מלא.

!!! success "פתרון - הטענה נכונה"
    יהי $a \in A$. צ"ל שקיימת $X \in \mathcal{P}(B)$ עם $\langle a, X \rangle \in S_{A,B}$.

    ניקח $X = \emptyset \in \mathcal{P}(B)$.

    מתקיים $a \notin \emptyset$, לכן $\langle a, \emptyset \rangle \in S_{A,B}$ ✓

---

### סעיף ב - יחס חד-ערכי (8 נק')

**שאלה:** הוכיחו או הפריכו: לכל שתי קבוצות $A, B$, אם $A \neq \emptyset$ ו-$S_{A,B}$ חד-ערכי, אז $B = \emptyset$.

!!! success "פתרון - הטענה נכונה"
    נניח $S_{A,B}$ חד-ערכי ו-$A \neq \emptyset$.

    נניח בשלילה $B \neq \emptyset$, אז קיים $b \in B$.

    יהי $a \in A$ (קיים כי $A \neq \emptyset$).

    אז:

    - $\langle a, \emptyset \rangle \in S_{A,B}$ (כי $a \notin \emptyset$)
    - $\langle a, \{b\} \rangle \in S_{A,B}$ (כי $a \neq b$ לא בהכרח, אבל $a \notin \{b\}$ כי $a \in A$ ו-$b \in B$ ו-$A, B$ זרות)

    **תיקון:** נבדוק מקרים:

    - אם $a \notin B$: $\langle a, \{b\} \rangle \in S_{A,B}$ ו-$\langle a, \emptyset \rangle \in S_{A,B}$, אבל $\{b\} \neq \emptyset$ - סתירה לחד-ערכיות
    - אם $a \in B$: אז $\langle a, \{a\} \rangle \notin S_{A,B}$, אבל $\langle a, \emptyset \rangle \in S_{A,B}$. אם קיים $b \neq a$ ב-$B$, אז $\langle a, \{b\} \rangle \in S_{A,B}$ - סתירה.

    בכל מקרה מגיעים לסתירה, לכן $B = \emptyset$ ✓

---

## טבלת סיכום

| מושג | הגדרה | שאלות |
|------|-------|-------|
| **רפלקסיבי** | $\forall a \in A. \langle a, a \rangle \in R$ | 2024Bb-1 |
| **סימטרי** | $\langle a, b \rangle \in R \Rightarrow \langle b, a \rangle \in R$ | 2024Ab-1 |
| **טרנזיטיבי** | $\langle a, b \rangle, \langle b, c \rangle \in R \Rightarrow \langle a, c \rangle \in R$ | 2024Ab-1 |
| **מלא** | $\forall a \in A. \exists b. \langle a, b \rangle \in R$ | 2024Bb-2, 2025Aa-1 |
| **חד-ערכי** | $\langle a, b \rangle, \langle a, c \rangle \in R \Rightarrow b = c$ | 2024Bb-2, 2025Aa-1 |
| **הרכבה** | $S \circ T = \{\langle a, c \rangle \mid \exists b. \langle a, b \rangle \in T \land \langle b, c \rangle \in S\}$ | 2024Ab-1, 2024Bb-2 |

---

## טיפים

!!! tip "טיפים לשאלות יחסים"
    1. **הוכחת תכונה:** בדקו ההגדרה המדויקת וכתבו "יהי/יהיו..."
    2. **הפרכה:** מספיקה דוגמה נגדית אחת קטנה
    3. **הרכבה:** זכרו $(S \circ T)(a) = S(T(a))$ - קודם $T$, אח"כ $S$
    4. **יחס מלא:** לכל איבר בתחום יש לפחות זוג אחד
    5. **יחס חד-ערכי:** לכל איבר בתחום יש לכל היותר זוג אחד
