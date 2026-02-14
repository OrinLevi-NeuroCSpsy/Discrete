# יחידה 13: חשבון עוצמות, איחוד בן מניה

## חשבון עוצמות - המשך

### תכונות מיוחדות לעוצמות אינסופיות

!!! abstract "טענה: חיבור עוצמות אינסופיות"
    לכל עוצמה אינסופית $a$:
    $$a + \aleph_0 = a$$

!!! abstract "טענה: כפל עוצמות אינסופיות"
    לכל עוצמה אינסופית $a$:
    $$a \cdot \aleph_0 = a$$

    ובפרט:
    $$\aleph_0 \cdot \aleph_0 = \aleph_0$$
    $$\aleph \cdot \aleph = \aleph$$

### חישובים חשובים

!!! info "עוצמות נפוצות"
    | ביטוי | תוצאה | הסבר |
    |-------|--------|-------|
    | $\aleph_0 + \aleph_0$ | $\aleph_0$ | $\mathbb{N} \cup \mathbb{N} \sim \mathbb{N}$ |
    | $\aleph_0 \cdot \aleph_0$ | $\aleph_0$ | $\mathbb{N} \times \mathbb{N} \sim \mathbb{N}$ |
    | $2^{\aleph_0}$ | $\aleph$ | $\mathcal{P}(\mathbb{N}) \sim \mathbb{R}$ |
    | $\aleph + \aleph$ | $\aleph$ | $\mathbb{R} \cup \mathbb{R} \sim \mathbb{R}$ |
    | $\aleph \cdot \aleph$ | $\aleph$ | $\mathbb{R} \times \mathbb{R} \sim \mathbb{R}$ |
    | $\aleph^{\aleph_0}$ | $\aleph$ | $(\mathbb{N} \to \mathbb{R}) \sim \mathbb{R}$ |
    | $2^{\aleph}$ | $> \aleph$ | משפט קנטור |

---

## איחוד בן מניה

### המשפט המרכזי

!!! abstract "משפט: איחוד בן מניה"
    יהי $\{A_i \mid i \in I\}$ אוסף **לכל היותר בן מניה** ($|I| \leq \aleph_0$) של קבוצות **לכל היותר בנות מניה** ($|A_i| \leq \aleph_0$ לכל $i \in I$).

    אזי האיחוד $\bigcup_{i \in I} A_i$ הוא **לכל היותר בן מניה**:
    $$\left| \bigcup_{i \in I} A_i \right| \leq \aleph_0$$

!!! note "מקרה פרטי"
    איחוד בן מניה של קבוצות בנות מניה הוא בן מניה.

### יישומים

!!! example "דוגמה 1: $\mathbb{Q}$ בת מניה"
    $$\mathbb{Q} = \bigcup_{n \in \mathbb{Z} \setminus \{0\}} \left\{ \frac{m}{n} \mid m \in \mathbb{Z} \right\}$$

    - $\mathbb{Z} \setminus \{0\}$ בת מניה (אינדקס בן מניה)
    - לכל $n$, הקבוצה $\left\{ \frac{m}{n} \mid m \in \mathbb{Z} \right\}$ בת מניה
    - לכן $\mathbb{Q}$ בת מניה

!!! example "דוגמה 2: איחוד קבוצות אלגבריות"
    קבוצת כל המספרים האלגבריים (שורשים של פולינומים עם מקדמים שלמים) היא בת מניה.

    - קבוצת הפולינומים עם מקדמים שלמים היא בת מניה
    - לכל פולינום יש מספר סופי של שורשים
    - לכן איחוד כל השורשים הוא בן מניה

---

## שימושים בחשבון עוצמות

### דוגמה: מחרוזות בינאריות

!!! example "עוצמת מחרוזות בינאריות מיוחדות"
    מצאו את עוצמת המחרוזות הבינאריות האינסופיות בהן 1 לא מופיע פעמיים ברצף.

    **פתרון**: נסמן את הקבוצה ב-$A$.

    **חסם עליון**: $A \subseteq \mathbb{N} \to \{0,1\}$, לכן:
    $$|A| \leq |\mathbb{N} \to \{0,1\}| = 2^{\aleph_0}$$

    **חסם תחתון**: נגדיר $F \in (\mathbb{N}_{\text{even}} \to \{0,1\}) \to A$ ע"י:
    $$F = \lambda g \in \mathbb{N}_{\text{even}} \to \{0,1\}. \lambda n \in \mathbb{N}. \begin{cases} g(n) & n \in \mathbb{N}_{\text{even}} \\ 0 & n \in \mathbb{N}_{\text{odd}} \end{cases}$$

    $F$ חח"ע, לכן $|A| \geq |\mathbb{N}_{\text{even}} \to \{0,1\}| = 2^{\aleph_0}$.

    מקש"ב: $|A| = 2^{\aleph_0}$.

### דוגמה: פונקציות מיוחדות

!!! example "עוצמת פונקציות חח\"ע עם תמונה בת מניה"
    חשבו את עוצמת הקבוצה:
    $$A = \{f \in \mathbb{N} \to \mathcal{P}(\mathbb{N}) \mid (\forall n. |f(n)| = \aleph_0) \land (f \text{ חח"ע})\}$$

    **פתרון**: נוכיח $|A| = 2^{\aleph_0}$.

    **חסם עליון**: $A \subseteq \mathbb{N} \to \mathcal{P}(\mathbb{N})$, לכן:
    $$|A| \leq |\mathbb{N} \to \mathcal{P}(\mathbb{N})| = |\mathcal{P}(\mathbb{N})|^{|\mathbb{N}|} = (2^{\aleph_0})^{\aleph_0} = 2^{\aleph_0 \cdot \aleph_0} = 2^{\aleph_0}$$

    **חסם תחתון**: נגדיר $F \in \mathcal{P}(\mathbb{N}_{\text{odd}}) \to A$ ע"י:
    $$F = \lambda T \in \mathcal{P}(\mathbb{N}_{\text{odd}}). \lambda n \in \mathbb{N}. T \cup (\mathbb{N}_{\text{even}} \setminus \{2n\})$$

    $F$ חח"ע, לכן $|A| \geq |\mathcal{P}(\mathbb{N}_{\text{odd}})| = 2^{\aleph_0}$.

    מקש"ב: $|A| = 2^{\aleph_0}$.

---

## אקסיומת הבחירה (העשרה)

### הגדרה

!!! info "הגדרה: פונקציית בחירה"
    תהי $X$ קבוצה שאיבריה הם קבוצות לא-ריקות.
    **פונקציית בחירה** היא פונקציה $f \in X \to \bigcup X$ המקיימת:
    $$\forall A \in X. f(A) \in A$$

    הרעיון: לכל איבר $A$ של $X$, הפונקציה "בוחרת" איבר $f(A)$ מתוך $A$.

!!! abstract "אקסיומת הבחירה"
    תהי $X$ קבוצה שאיבריה הם קבוצות לא ריקות. אז קיימת פונקציית בחירה $f \in X \to \bigcup X$.

### דוגמאות

!!! example "דוגמה: קבוצות סופיות"
    עבור $X = \{\{1,2,3\}, \{4,5\}\}$:

    - $\bigcup X = \{1,2,3,4,5\}$
    - פונקציית בחירה אפשרית: $f(\{1,2,3\}) = 2$, $f(\{4,5\}) = 4$

!!! example "דוגמה: תתי-קבוצות של $\mathbb{N}$"
    עבור $X = \mathcal{P}(\mathbb{N}) \setminus \{\emptyset\}$:

    ניתן להגדיר $f = \lambda A \in X. \min(A)$ (בלי אקסיומת הבחירה!)

!!! warning "מתי צריך את האקסיומה?"
    עבור $X = \mathcal{P}(\mathbb{R}) \setminus \{\emptyset\}$, לא ניתן להגדיר פונקציית בחירה במפורש (אין מינימום ב-$\mathbb{R}$).

    אקסיומת הבחירה מבטיחה שקיימת פונקציה כזו, מבלי להגדיר אותה במפורש.

---

## סיכום היחידה

!!! abstract "נקודות מפתח"
    1. **איחוד בן מניה**: איחוד של לכל היותר $\aleph_0$ קבוצות בנות מניה הוא בן מניה
    2. **חשבון עוצמות**: $\aleph_0 \cdot \aleph_0 = \aleph_0$, $\aleph \cdot \aleph = \aleph$
    3. **שיטת קש"ב**: למציאת עוצמה - מוצאים חסם עליון ותחתון שווים
    4. **אקסיומת הבחירה**: מבטיחה קיום פונקציית בחירה לכל קבוצת קבוצות לא-ריקות

---

## תרגילים

!!! example "תרגיל 1"
    הוכיחו שקבוצת הפולינומים עם מקדמים רציונליים היא בת מניה.

!!! example "תרגיל 2"
    חשבו את $\aleph_0^{\aleph_0}$.

!!! example "תרגיל 3"
    הוכיחו ש-$|\mathbb{R}^n| = \aleph$ לכל $n \geq 1$.

---

## מקורות

!!! note "מקורות היחידה"
    - ספר הקורס: פרק ג.5 - חשבון עוצמות
    - תרגול 13 - חשבון עוצמות, איחוד בן מניה
