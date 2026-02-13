# תרגילי יחסים

## תרגיל 1 - תכונות יחסים

**שאלה:** יהי $R$ יחס על $\mathbb{N}$ המוגדר: $nRm \iff n + m$ זוגי.

קבעו האם $R$ רפלקסיבי, סימטרי, אנטי-סימטרי, טרנזיטיבי.

??? success "פתרון"
    **רפלקסיבי:** כן. $n + n = 2n$ תמיד זוגי. $\checkmark$

    **סימטרי:** כן. $n + m = m + n$, אז אם $nRm$ אז $mRn$. $\checkmark$

    **אנטי-סימטרי:** לא. $1R3$ ו-$3R1$ (כי $1+3=4$ זוגי), אבל $1 \neq 3$.

    **טרנזיטיבי:** כן. אם $n+m$ זוגי ו-$m+k$ זוגי, אז:
    - $n, m$ שניהם זוגיים או שניהם אי-זוגיים
    - $m, k$ שניהם זוגיים או שניהם אי-זוגיים
    - לכן $n, k$ מאותה זוגיות, ו-$n+k$ זוגי. $\checkmark$

!!! info "מסקנה"
    $R$ הוא יחס שקילות (רפלקסיבי, סימטרי, טרנזיטיבי).

---

## תרגיל 2 - הרכבת יחסים

**שאלה:** יהיו $R, S$ יחסים על קבוצה $A$. הוכיחו: אם $R \subseteq S$ אז לכל $n \in \mathbb{N}$: $R^{(n)} \subseteq S^{(n)}$.

??? success "פתרון"
    **באינדוקציה על $n$.**

    **בסיס:** $n = 0$.
    $$R^{(0)} = I_A = S^{(0)} \checkmark$$

    **צעד:** נניח $R^{(n)} \subseteq S^{(n)}$ ונוכיח ל-$n+1$.

    יהי $\langle a, b \rangle \in R^{(n+1)} = R^{(n)} \circ R$.

    קיים $x \in A$ כך ש-$\langle a, x \rangle \in R$ ו-$\langle x, b \rangle \in R^{(n)}$.

    מ-$R \subseteq S$: $\langle a, x \rangle \in S$.

    מהנחת האינדוקציה: $\langle x, b \rangle \in S^{(n)}$.

    מהגדרת הרכבה: $\langle a, b \rangle \in S^{(n)} \circ S = S^{(n+1)}$. $\checkmark$

---

## תרגיל 3 - הסגור הטרנזיטיבי

**הגדרה:** לכל יחס $R$, הסגור הטרנזיטיבי שלו הוא:
$$R^+ = \bigcup_{i \in \mathbb{N}^+} R^{(i)}$$

**שאלה:** עבור $R = \{\langle n, n+1 \rangle \mid n \in \mathbb{N}\}$, מהו $R^+$?

??? success "פתרון"
    **טענה:** $R^+ = R_< = \{\langle x, y \rangle \in \mathbb{N}^2 \mid x < y\}$

    **טענת עזר:** לכל $i \in \mathbb{N}^+$: $R^{(i)} = \{\langle n, n+i \rangle \mid n \in \mathbb{N}\}$.

    *הוכחה באינדוקציה:*

    - **בסיס:** $i = 1$: $R^{(1)} = R = \{\langle n, n+1 \rangle \mid n \in \mathbb{N}\}$. $\checkmark$

    - **צעד:** $R^{(i)} = R^{(i-1)} \circ R$.

      $xR^{(i)}y$ אמ"מ קיים $z$ עם $xRz$ ו-$zR^{(i-1)}y$.

      אמ"מ (I.H.) קיים $z$ עם $z = x+1$ ו-$y = z + (i-1)$.

      אמ"מ $y = x + i$. $\checkmark$

    **הוכחת $R^+ = R_<$:**

    - **כיוון $\subseteq$:** אם $\langle x, y \rangle \in R^+$, קיים $i$ עם $\langle x, y \rangle \in R^{(i)}$, לכן $y = x + i$ ובפרט $x < y$.

    - **כיוון $\supseteq$:** אם $x < y$, אז $y = x + (y-x)$ ו-$y-x \in \mathbb{N}^+$, לכן $\langle x, y \rangle \in R^{(y-x)} \subseteq R^+$.

---

## תרגיל 4 - יחס הפוך והרכבה

**שאלה:** יהיו $R \subseteq A \times B$ ו-$S \subseteq B \times C$ יחסים. הוכיחו:
$$(S \circ R)^{-1} = R^{-1} \circ S^{-1}$$

??? success "פתרון"
    $$\langle c, a \rangle \in (S \circ R)^{-1}$$

    $$\iff \langle a, c \rangle \in S \circ R$$

    $$\iff \exists b \in B. \langle a, b \rangle \in R \land \langle b, c \rangle \in S$$

    $$\iff \exists b \in B. \langle b, a \rangle \in R^{-1} \land \langle c, b \rangle \in S^{-1}$$

    $$\iff \langle c, a \rangle \in R^{-1} \circ S^{-1} \checkmark$$

!!! warning "שימו לב לסדר!"
    $(S \circ R)^{-1} = R^{-1} \circ S^{-1}$ - הסדר מתהפך!

---

## תרגיל 5 - יחס שקילות ומחלקות

**שאלה:** יהי $R$ על $\mathbb{Z}$ המוגדר: $aRb \iff 3 | (a - b)$.

1. הוכיחו ש-$R$ יחס שקילות.
2. מצאו את מחלקות השקילות.

??? success "פתרון"
    **חלק 1:**

    - **רפלקסיבי:** $a - a = 0$ מתחלק ב-3. $\checkmark$

    - **סימטרי:** אם $3 | (a-b)$ אז $3 | (-(a-b)) = (b-a)$. $\checkmark$

    - **טרנזיטיבי:** אם $3 | (a-b)$ ו-$3 | (b-c)$, אז $3 | ((a-b) + (b-c)) = (a-c)$. $\checkmark$

    ---

    **חלק 2:**

    יש 3 מחלקות שקילות:

    $$[0]_R = \{..., -6, -3, 0, 3, 6, 9, ...\} = 3\mathbb{Z}$$

    $$[1]_R = \{..., -5, -2, 1, 4, 7, 10, ...\} = 3\mathbb{Z} + 1$$

    $$[2]_R = \{..., -4, -1, 2, 5, 8, 11, ...\} = 3\mathbb{Z} + 2$$

    קבוצת המנה: $\mathbb{Z}/R = \{[0]_R, [1]_R, [2]_R\}$

---

## טבלת תכונות יחסים

| תכונה | הגדרה | סימון |
|-------|-------|-------|
| **רפלקסיבי** | $\forall a. aRa$ | $I_A \subseteq R$ |
| **סימטרי** | $aRb \Rightarrow bRa$ | $R = R^{-1}$ |
| **אנטי-סימטרי** | $aRb \land bRa \Rightarrow a = b$ | $R \cap R^{-1} \subseteq I_A$ |
| **טרנזיטיבי** | $aRb \land bRc \Rightarrow aRc$ | $R \circ R \subseteq R$ |
| **מלא (קשר)** | $\forall a, b. aRb \lor bRa$ | |

---

## טיפים

!!! tip "טיפים לתרגילי יחסים"
    1. **בדיקת תכונות:** בדקו כל תכונה בנפרד
    2. **הפרכה:** מספיקה דוגמה נגדית אחת
    3. **הרכבה:** זכרו $(S \circ R) = \{(a,c) \mid \exists b. aRb \land bSc\}$
    4. **יחס הפוך:** $\langle a, b \rangle \in R^{-1} \iff \langle b, a \rangle \in R$
    5. **מחלקות שקילות:** כל איבר שייך למחלקה אחת בדיוק
