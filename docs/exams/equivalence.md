# שאלות מבחן בנושא יחסי שקילות

## מבחן 2024 מועד א - שאלה 3ג

### חלוקה גוררת יחס שקילות

**הגדרה:** בהינתן $f \in \mathbb{N} \to \mathcal{P}(\mathbb{N})$ נגדיר:
$$R_f = \{\langle n, m \rangle \in \mathbb{N}^2 \mid f(n) \subseteq f(m)\}$$

**טענה:** אם $\text{Im}(f)$ היא חלוקה של $\mathbb{N}$, אז $R_f$ הוא יחס שקילות.

!!! success "פתרון - הטענה נכונה"
    ידוע ש-$R_f$ רפלקסיבי וטרנזיטיבי. נוכיח סימטריות:

    יהיו $n, m$ עם $\langle n, m \rangle \in R_f$, כלומר $f(n) \subseteq f(m)$.

    מ-$\text{Im}(f)$ חלוקה: $f(n) \neq \emptyset$, לכן קיים $k \in f(n)$.

    מ-$f(n) \subseteq f(m)$: $k \in f(m)$, לכן $f(n) \cap f(m) \neq \emptyset$.

    מזרות החלוקה: $f(n) = f(m)$, ובפרט $f(m) \subseteq f(n)$.

    לכן $\langle m, n \rangle \in R_f$ ✓

!!! warning "טעות נפוצה"
    חייבים להשתמש בכך שבחלוקה **אין חלקים ריקים**!

---

## מבחן 2024 מועד א - שאלה 5

### יחס שקילות על פונקציות

**הגדרה:** $S = \{\langle f, g \rangle \in (\mathbb{R} \to \mathbb{R})^2 \mid f^{-1}[\{1\}] = g^{-1}[\{1\}]\}$

---

### סעיף א - מחלקת שקילות סופית (3 נק')

**שאלה:** הציגו $f$ עבורה $[f]_S$ סופית.

!!! success "פתרון"
    $$f = \lambda x \in \mathbb{R}. 1$$

    זו הפונקציה **היחידה** עבורה $|[f]_S| = 1$.

---

### סעיף ב - אין מחלקה בת מנייה (8 נק')

**שאלה:** הוכיחו שלא קיימת $f$ עבורה $|[f]_S| = \aleph_0$.

!!! success "פתרון"
    תהי $f \in \mathbb{R} \to \mathbb{R}$.

    **מקרה 1:** $f = \lambda x. 1$ - אז $|[f]_S| = 1$ (סופית).

    **מקרה 2:** קיים $x_0$ עם $f(x_0) \neq 1$.

    נגדיר $F \in (0,1) \to [f]_S$:

    $$F(a) = \lambda x \in \mathbb{R}. \begin{cases} f(x) & x \neq x_0 \\ a & x = x_0 \end{cases}$$

    **$F(a) \in [f]_S$:** צ"ל $(F(a))^{-1}[\{1\}] = f^{-1}[\{1\}]$

    - $x \in f^{-1}[\{1\}] \Rightarrow f(x) = 1 \Rightarrow x \neq x_0 \Rightarrow (F(a))(x) = f(x) = 1$
    - $x \in (F(a))^{-1}[\{1\}] \Rightarrow (F(a))(x) = 1$. כיוון ש-$(F(a))(x_0) = a \neq 1$, אז $x \neq x_0$, לכן $f(x) = 1$

    **$F$ חח"ע:** $F(a) = F(b) \Rightarrow (F(a))(x_0) = (F(b))(x_0) \Rightarrow a = b$

    לכן $|[f]_S| \geq |(0,1)| = \aleph$. בשני המקרים $|[f]_S| \neq \aleph_0$.

---

### סעיף ג - עוצמת קבוצת המנה (9 נק')

**שאלה:** חשבו את $|(\mathbb{R} \to \mathbb{R})/S|$.

!!! success "פתרון: $2^\aleph$"
    נגדיר $G \in \mathcal{P}(\mathbb{R}) \to (\mathbb{R} \to \mathbb{R})/S$:

    $$G(A) = [\chi_A]_S$$

    כאשר $\chi_A = \lambda x \in \mathbb{R}. \begin{cases} 1 & x \in A \\ 0 & x \notin A \end{cases}$

    **$G$ חח"ע:** $G(A_1) = G(A_2) \Rightarrow [\chi_{A_1}]_S = [\chi_{A_2}]_S$

    $\Rightarrow \chi_{A_1}^{-1}[\{1\}] = \chi_{A_2}^{-1}[\{1\}] \Rightarrow A_1 = A_2$

    **$G$ על:** לכל $[f]_S$, ניקח $A = f^{-1}[\{1\}]$, אז $G(A) = [f]_S$

    לכן $|(\mathbb{R} \to \mathbb{R})/S| = |\mathcal{P}(\mathbb{R})| = 2^\aleph$

---

## מבחן 2023 מועד א - שאלה 1

### יחס שקילות מבוסס תמונה

**הגדרה:** $S$ על $\mathbb{R} \to \mathbb{N}$:
$$fSg \iff \text{Im}(f) = \text{Im}(g)$$

---

### סעיף א - עוצמת מחלקה ספציפית (5 נק')

**שאלה:** מהי עוצמת $[\lambda r \in \mathbb{R}. 5]_S$?

!!! success "פתרון: 1"
    נסמן $f = \lambda r. 5$. העוצמה לפחות 1 כי $f \in [f]_S$.

    תהי $g \in [f]_S$. נניח $g \neq f$, אז קיים $r_1$ עם $g(r_1) \neq 5$.

    לכן $\text{Im}(g) \neq \{5\} = \text{Im}(f)$, סתירה ל-$g \in [f]_S$.

    לכן $|[f]_S| = 1$.

---

### סעיף ב - זיווג (8 נק')

**שאלה:** יהי $X$ = מחלקות שקילות אינסופיות. הראו:
$$X \sim \{A \in \mathcal{P}(\mathbb{N}) \mid |A| \geq 2\}$$

!!! success "פתרון"
    $$F = \lambda [f] \in X. \text{Im}(f)$$

    $$F^{-1} = \lambda A \in \mathcal{P}_{\geq 2}(\mathbb{N}). \left[\lambda x \in \mathbb{R}. \begin{cases} x & x \in A \\ \min A & \text{אחרת} \end{cases}\right]$$

---

### סעיף ג - עוצמת $X$ (4 נק')

**שאלה:** חשבו את עוצמת $X$.

!!! success "פתרון: $2^{\aleph_0} = \aleph$"
    מסעיף ב: $|X| = |\mathcal{P}_{\geq 2}(\mathbb{N})|$

    **חסם עליון:** $\mathcal{P}_{\geq 2}(\mathbb{N}) \subseteq \mathcal{P}(\mathbb{N})$, לכן $|X| \leq 2^{\aleph_0}$

    **חסם תחתון:** נגדיר $F \in \mathcal{P}(\mathbb{N}_{even}) \to \mathcal{P}_{\geq 2}(\mathbb{N})$:

    $$F(A) = A \cup \mathbb{N}_{odd}$$

    $F$ חח"ע כי $F(A) \cap \mathbb{N}_{even} = A$.

    לכן $|X| \geq |\mathcal{P}(\mathbb{N}_{even})| = 2^{\aleph_0}$

    **מקש"ב:** $|X| = 2^{\aleph_0}$

---

## טבלת מושגים

| מושג | הגדרה | שאלות |
|------|-------|-------|
| **מחלקת שקילות** | $[x]_E = \{y \mid xEy\}$ | 2024-5, 2023-1 |
| **קבוצת מנה** | $A/E = \{[x]_E \mid x \in A\}$ | 2024-5ג |
| **חלוקה** | כיסוי זר | 2024-3ג |
| **אי-תלות בנציג** | הגדרה לא תלויה בבחירת נציג | 2024-5ג |

---

## טיפים

!!! tip "טיפים לשאלות יחסי שקילות"
    1. **הוכחת יחס שקילות:** רפלקסיביות + סימטריה + טרנזיטיביות
    2. **מחלקות שוות או זרות:** $[x] = [y]$ או $[x] \cap [y] = \emptyset$
    3. **קבוצת מנה:** אוסף כל המחלקות השונות
    4. **זיווג עם קבוצת מנה:** לעתים קרובות דרך פונקציה אופיינית
