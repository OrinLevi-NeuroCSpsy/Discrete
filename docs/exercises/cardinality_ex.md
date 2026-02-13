# תרגילי עוצמות

## תרגיל 1 - זיווג בסיסי

**שאלה:** הוכיחו ש-$\mathbb{N}_{even} \sim \mathbb{N}$.

??? success "פתרון"
    נגדיר $f: \mathbb{N} \to \mathbb{N}_{even}$ ע"י $f(n) = 2n$.

    **$f$ חח"ע:** אם $f(n_1) = f(n_2)$ אז $2n_1 = 2n_2$, לכן $n_1 = n_2$. $\checkmark$

    **$f$ על:** לכל $m \in \mathbb{N}_{even}$, קיים $n = \frac{m}{2} \in \mathbb{N}$ כך ש-$f(n) = 2 \cdot \frac{m}{2} = m$. $\checkmark$

    לכן $f$ זיווג, ו-$\mathbb{N}_{even} \sim \mathbb{N}$.

---

## תרגיל 2 - קש"ב (קנטור-שרדר-ברנשטיין)

**שאלה:** הוכיחו ש-$|(0,1)| = |\mathbb{R}|$.

??? success "פתרון"
    **חסם עליון:** $(0,1) \subseteq \mathbb{R}$, לכן $|(0,1)| \leq |\mathbb{R}|$.

    **חסם תחתון:** נגדיר $g: \mathbb{R} \to (0,1)$ ע"י:

    $$g(x) = \frac{1}{1 + e^{-x}}$$

    (פונקציית הסיגמואיד)

    $g$ רציפה ומונוטונית עולה, $\lim_{x \to -\infty} g(x) = 0$, $\lim_{x \to \infty} g(x) = 1$.

    לכן $g$ חח"ע מ-$\mathbb{R}$ ל-$(0,1)$, ומכאן $|\mathbb{R}| \leq |(0,1)|$.

    **מקש"ב:** $|(0,1)| = |\mathbb{R}| = \aleph$. $\checkmark$

---

## תרגיל 3 - לכסון (דיאגונליזציה)

**שאלה:** הוכיחו ש-$\mathcal{P}(\mathbb{N})$ אינה בת מנייה.

??? success "פתרון"
    נניח בשלילה שקיים זיווג $f: \mathbb{N} \to \mathcal{P}(\mathbb{N})$.

    נגדיר את "הקבוצה האלכסונית":

    $$D = \{n \in \mathbb{N} \mid n \notin f(n)\}$$

    $D \subseteq \mathbb{N}$, לכן $D \in \mathcal{P}(\mathbb{N})$.

    מ-$f$ על, קיים $k \in \mathbb{N}$ כך ש-$f(k) = D$.

    **שאלה:** האם $k \in D$?

    - אם $k \in D$: מהגדרת $D$, $k \notin f(k) = D$. **סתירה!**
    - אם $k \notin D$: מהגדרת $D$, $k \in D$. **סתירה!**

    לכן לא קיים זיווג, ו-$|\mathcal{P}(\mathbb{N})| > |\mathbb{N}| = \aleph_0$.

---

## תרגיל 4 - חשבון עוצמות

**שאלה:** חשבו את $|\mathbb{N} \to \mathbb{N}|$.

??? success "פתרון"
    **חסם עליון:**

    $$|\mathbb{N} \to \mathbb{N}| = |\mathbb{N}|^{|\mathbb{N}|} = \aleph_0^{\aleph_0}$$

    נראה ש-$\aleph_0^{\aleph_0} \leq 2^{\aleph_0}$:

    $$\aleph_0^{\aleph_0} \leq (2^{\aleph_0})^{\aleph_0} = 2^{\aleph_0 \cdot \aleph_0} = 2^{\aleph_0}$$

    ---

    **חסם תחתון:**

    נגדיר $g: \mathcal{P}(\mathbb{N}) \to (\mathbb{N} \to \mathbb{N})$ ע"י:

    $$g(A) = \chi_A = \lambda n \in \mathbb{N}. \begin{cases} 1 & n \in A \\ 0 & n \notin A \end{cases}$$

    $g$ חח"ע (פונקציות אופייניות שונות לקבוצות שונות).

    לכן $|\mathbb{N} \to \mathbb{N}| \geq |\mathcal{P}(\mathbb{N})| = 2^{\aleph_0}$.

    ---

    **מקש"ב:** $|\mathbb{N} \to \mathbb{N}| = 2^{\aleph_0} = \aleph$

---

## תרגיל 5 - בניית זיווג

**שאלה:** הוכיחו ש-$\mathbb{Q}$ בת מנייה.

??? success "פתרון"
    נגדיר $f: \mathbb{Q} \to \mathbb{Z} \times \mathbb{N}^+$ ע"י:

    $$f\left(\frac{p}{q}\right) = (p, q)$$

    כאשר $\frac{p}{q}$ בצורה מצומצמת עם $q > 0$.

    $f$ חח"ע (ייצוג יחיד בצורה מצומצמת).

    לכן $|\mathbb{Q}| \leq |\mathbb{Z} \times \mathbb{N}^+| = \aleph_0 \cdot \aleph_0 = \aleph_0$.

    מ-$\mathbb{N} \subseteq \mathbb{Q}$: $|\mathbb{Q}| \geq \aleph_0$.

    **מקש"ב:** $|\mathbb{Q}| = \aleph_0$. $\checkmark$

---

## תרגיל 6 - משפט קנטור

**שאלה:** הוכיחו ש-$|A| < |\mathcal{P}(A)|$ לכל קבוצה $A$.

??? success "פתרון"
    **$|A| \leq |\mathcal{P}(A)|$:**

    $f: A \to \mathcal{P}(A)$ המוגדרת $f(a) = \{a\}$ היא חח"ע. $\checkmark$

    ---

    **$|A| \neq |\mathcal{P}(A)|$:**

    נניח בשלילה שקיים זיווג $g: A \to \mathcal{P}(A)$.

    נגדיר $D = \{a \in A \mid a \notin g(a)\}$.

    $D \in \mathcal{P}(A)$, לכן קיים $x \in A$ עם $g(x) = D$.

    - אם $x \in D$: מהגדרת $D$, $x \notin g(x) = D$. **סתירה!**
    - אם $x \notin D$: מהגדרת $D$, $x \in D$. **סתירה!**

    לכן אין זיווג, ו-$|A| < |\mathcal{P}(A)|$. $\checkmark$

---

## טבלת עוצמות חשובות

| קבוצה | עוצמה |
|-------|-------|
| $\mathbb{N}, \mathbb{Z}, \mathbb{Q}$ | $\aleph_0$ |
| $\mathbb{R}, (0,1), \mathcal{P}(\mathbb{N})$ | $\aleph = 2^{\aleph_0}$ |
| $\mathbb{N} \to \mathbb{N}$ | $\aleph = 2^{\aleph_0}$ |
| $\mathcal{P}(\mathbb{R})$ | $2^\aleph$ |
| $A \times B$ (אינסופיות) | $\max(|A|, |B|)$ |
| $A \to B$ | $|B|^{|A|}$ |

---

## טיפים

!!! tip "טיפים לתרגילי עוצמות"
    1. **זיווג:** בנו פונקציה חח"ע ועל
    2. **קש"ב:** הראו $|A| \leq |B|$ ו-$|B| \leq |A|$
    3. **לכסון:** בנו איבר שונה מכל איבר בתמונה "באלכסון"
    4. **חשבון:** $\aleph_0 \cdot \aleph_0 = \aleph_0$, $\aleph \cdot \aleph = \aleph$, $2^{\aleph_0} = \aleph$
    5. **קנטור:** $2^a > a$ לכל עוצמה $a$
