# תרגילי פונקציות

## תרגיל 1 - יחסים חד-ערכיים ומלאים

**שאלה:** הוכיחו או הפריכו:

1. היחס $R = \{\langle n, y \rangle \in \mathbb{N}^+ \times \mathbb{R} \mid n^2 + y^2 = 5\}$ הוא חד-ערכי.
2. היחס $R = \{\langle n, y \rangle \in \mathbb{N}^+ \times \mathbb{R} \mid n^2 + y^2 = 5\}$ הוא מלא ב-$\mathbb{N}^+$.
3. היחס $R = \{\langle n, y \rangle \in \mathbb{N}^+ \times \mathbb{R} \mid n^2 + y^2 = 1\}$ הוא חד-ערכי.

??? success "פתרון"
    **1. לא נכון.** $\langle 1, 2 \rangle \in R$ וגם $\langle 1, -2 \rangle \in R$.

    (כי $1^2 + 2^2 = 5$ וגם $1^2 + (-2)^2 = 5$)

    ---

    **2. לא נכון.** עבור $n = 5$, אין $y$ ממשי המקיים $25 + y^2 = 5$.

    (כי $y^2 = -20 < 0$ - אין פתרון ממשי)

    ---

    **3. נכון.** $R = \{\langle 1, 0 \rangle\}$ - יש רק זוג אחד!

    עבור $n = 1$: $1 + y^2 = 1 \Rightarrow y = 0$.

    עבור $n \geq 2$: $n^2 \geq 4 > 1$, אז אין פתרון.

---

## תרגיל 2 - הרכבה ויחס הופכי

**שאלה:** הוכיחו או הפריכו: לכל יחס $R$ על קבוצה $A$: $R \circ R^{-1} \subseteq I_A$.

??? danger "פתרון - לא נכון"
    **דוגמה נגדית:**

    $R = \{\langle 1, 2 \rangle, \langle 1, 3 \rangle\} \subseteq \mathbb{N} \times \mathbb{N}$

    אז $R^{-1} = \{\langle 2, 1 \rangle, \langle 3, 1 \rangle\}$

    $R \circ R^{-1}$: מחפשים $\langle a, c \rangle$ כך שקיים $b$ עם $\langle a, b \rangle \in R^{-1}$ ו-$\langle b, c \rangle \in R$.

    - $\langle 2, 1 \rangle \in R^{-1}$ ו-$\langle 1, 3 \rangle \in R$ $\Rightarrow$ $\langle 2, 3 \rangle \in R \circ R^{-1}$

    אבל $\langle 2, 3 \rangle \notin I_\mathbb{N}$ כי $2 \neq 3$!

---

## תרגיל 3 - תנאי להכלה ביחס הזהות

**שאלה:** יהי יחס $R$ על קבוצה $A$. מצאו תנאי הכרחי ומספיק על $R$ לכך ש-$R \circ R^{-1} \subseteq I_A$.

??? success "פתרון"
    **התנאי:** $R$ חד-ערכי.

    **מספיקות:** נניח $R$ חד-ערכי. יהי $\langle a, b \rangle \in R \circ R^{-1}$.

    קיים $x \in A$ כך ש-$\langle a, x \rangle \in R^{-1}$ ו-$\langle x, b \rangle \in R$.

    מהגדרת יחס הופכי: $\langle x, a \rangle \in R$.

    מ-$R$ חד-ערכי ו-$\langle x, a \rangle, \langle x, b \rangle \in R$: $a = b$.

    לכן $\langle a, b \rangle = \langle a, a \rangle \in I_A$. $\checkmark$

    **הכרחיות:** נניח $R \circ R^{-1} \subseteq I_A$. יהיו $a, b, c \in A$ עם $\langle a, b \rangle, \langle a, c \rangle \in R$.

    מהגדרת יחס הופכי: $\langle b, a \rangle \in R^{-1}$.

    מהגדרת הרכבה: $\langle b, c \rangle \in R \circ R^{-1}$.

    מההנחה: $\langle b, c \rangle \in I_A$, לכן $b = c$.

    $R$ חד-ערכי. $\checkmark$

---

## תרגיל 4 - הרכבת יחסים חד-ערכיים

**שאלה:** יהיו $T \subseteq A \times B$ ו-$S \subseteq B \times C$ יחסים. הוכיחו שאם $S$ ו-$T$ חד-ערכיים אז גם $S \circ T$ חד-ערכי.

??? success "פתרון"
    יהיו $a \in A$, $c_1, c_2 \in C$ כך ש-$\langle a, c_1 \rangle \in S \circ T$ וגם $\langle a, c_2 \rangle \in S \circ T$.

    מהגדרת הרכבה:
    - קיים $b_1 \in B$ עם $\langle a, b_1 \rangle \in T$ ו-$\langle b_1, c_1 \rangle \in S$
    - קיים $b_2 \in B$ עם $\langle a, b_2 \rangle \in T$ ו-$\langle b_2, c_2 \rangle \in S$

    מ-$T$ חד-ערכי: $b_1 = b_2$ (נסמן $b$).

    לכן $\langle b, c_1 \rangle \in S$ ו-$\langle b, c_2 \rangle \in S$.

    מ-$S$ חד-ערכי: $c_1 = c_2$. $\checkmark$

!!! info "מסקנה"
    הרכבה של פונקציות היא פונקציה.

---

## תרגיל 5 - כתיב למבדא

**שאלה:** חשבו את הביטויים הבאים:

1. $(\lambda x \in \mathbb{N}. x^2 + 3)(5)$
2. $(\lambda x \in \mathbb{N}. \lambda y \in \mathbb{N}. x + y)(3)(4)$
3. $(\lambda f \in \mathbb{N} \to \mathbb{N}. f(f(1)))(\lambda x \in \mathbb{N}. x + 1)$

??? success "פתרון"
    **1.** $(\lambda x \in \mathbb{N}. x^2 + 3)(5) = 5^2 + 3 = 28$

    ---

    **2.** $(\lambda x \in \mathbb{N}. \lambda y \in \mathbb{N}. x + y)(3)(4)$

    $= (\lambda y \in \mathbb{N}. 3 + y)(4)$

    $= 3 + 4 = 7$

    ---

    **3.** $(\lambda f \in \mathbb{N} \to \mathbb{N}. f(f(1)))(\lambda x \in \mathbb{N}. x + 1)$

    נסמן $g = \lambda x \in \mathbb{N}. x + 1$

    $= g(g(1)) = g(1 + 1) = g(2) = 2 + 1 = 3$

---

## תרגיל 6 - הגדרת פונקציה עם יוטא

**שאלה:** הגדירו פונקציה $\min : \mathcal{P}(\mathbb{N}) \setminus \{\emptyset\} \to \mathbb{N}$ שמחזירה את המינימום של כל קבוצה.

??? success "פתרון"
    $$\min = \lambda A \in \mathcal{P}(\mathbb{N}) \setminus \{\emptyset\}. \iota a \in A. \forall x \in A. a \leq x$$

    **למה ההגדרה חוקית?**

    לכל $A \in \mathcal{P}(\mathbb{N}) \setminus \{\emptyset\}$ (קבוצה לא ריקה של טבעיים):

    - **קיום:** מעקרון הסדר הטוב, לכל קבוצה לא ריקה של טבעיים יש מינימום.
    - **יחידות:** אם $a_1, a_2$ שניהם מינימליים, אז $a_1 \leq a_2$ ו-$a_2 \leq a_1$, לכן $a_1 = a_2$.

    **דוגמה:** $\min(\mathbb{N}_{odd}) = 1$

---

## טבלת סיכום

| מושג | הגדרה |
|------|-------|
| **יחס חד-ערכי** | $\langle a, b_1 \rangle, \langle a, b_2 \rangle \in R \Rightarrow b_1 = b_2$ |
| **יחס מלא** | $\forall a \in A. \exists b \in B. \langle a, b \rangle \in R$ |
| **פונקציה** | יחס חד-ערכי ומלא |
| **תחום** | $\text{Dom}(f) = A$ |
| **תמונה** | $\text{Im}(f) = \{f(x) \mid x \in \text{Dom}(f)\}$ |
| **הרכבה** | $(g \circ f)(x) = g(f(x))$ |

---

## כללי תחשיב למבדא

| כלל | תיאור | נוסחה |
|-----|-------|-------|
| **$\alpha$ (אלפא)** | החלפת משתנה | $\lambda x \in A. t = \lambda y \in A. t(y/x)$ |
| **$\beta$ (בטא)** | הצבה | $(\lambda x \in A. t)(s) = t(s/x)$ |
| **$\eta$ (אטא)** | אקסטנציונליות | $\lambda x \in \text{Dom}(f). f(x) = f$ |

---

## טיפים

!!! tip "טיפים לתרגילי פונקציות"
    1. **בדיקת חד-ערכיות:** האם יש קלט עם שני פלטים שונים?
    2. **בדיקת מלאות:** האם לכל קלט יש פלט?
    3. **הרכבה:** זכרו $(g \circ f)(x) = g(f(x))$ - קודם $f$, אח"כ $g$
    4. **כתיב למבדא:** הציבו לפי כלל $\beta$
    5. **סימן יוטא:** ודאו קיום ויחידות!
