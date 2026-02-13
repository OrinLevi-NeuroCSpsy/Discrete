# יחידה 3: קבוצות

## מושגי יסוד

### מהי קבוצה?

!!! info "הגדרה: קבוצה"
    **קבוצה** (Set) היא אוסף של עצמים, המהווה עצם בעצמו. לעצמים שמרכיבים קבוצה קוראים **איברי** הקבוצה, ועל כל אחד מהם אומרים שהוא **שייך** לקבוצה.

**סימון:** אם \(t\) הוא איבר של קבוצה \(A\), נכתוב \(t \in A\). אם \(t\) אינו איבר של \(A\), נכתוב \(t \notin A\).

!!! note "נקודות חשובות"
    - **אין הגבלה** על מה שיכול לשמש כאיבר בקבוצה -- כל עצם יכול להיות איבר.
    - קבוצות אינן חייבות להיות **הומוגניות** -- ניתן לערבב סוגי עצמים שונים.
    - קבוצות יכולות להיות **סופיות** או **אינסופיות**.
    - קבוצות עצמן נחשבות לעצמים, ולכן **קבוצה יכולה להיות איבר של קבוצה אחרת**.

### עקרון האקסטנציונליות

!!! warning "עקרון האקסטנציונליות"
    שתי קבוצות הן **שוות** אם ורק אם יש להן **בדיוק אותם איברים**.

    בסימון פורמלי:
    $$A = B \Leftrightarrow \forall x.(x \in A \leftrightarrow x \in B)$$

**משמעות:** קבוצה נקבעת אך ורק על-ידי איבריה -- לא על-ידי סדר הצגתם, לא על-ידי האופן שבו תוארה, ולא על-ידי כל מאפיין אחר.

!!! example "דוגמאות"
    - \(\{1, 2, 3\} = \{3, 1, 2\} = \{1, 1, 2, 3\}\) -- סדר ההצגה וכפילויות לא משנים.
    - קבוצת המספרים הזוגיים בין 1 ל-5 שווה לקבוצה \(\{2, 4\}\).

---

## הכלה (תת-קבוצה)

### הגדרה

!!! info "הגדרה: הכלה"
    נאמר ש-\(A\) היא **תת-קבוצה** של \(B\) (או ש-\(A\) **חלקית** ל-\(B\), או ש-\(B\) **מכילה** את \(A\)) אם כל איבר של \(A\) הוא גם איבר של \(B\).

    **סימון:** \(A \subseteq B\)

    בסימון פורמלי:
    $$A \subseteq B \Leftrightarrow \forall x.(x \in A \rightarrow x \in B)$$

!!! info "הגדרה: הכלה ממש"
    נאמר ש-\(A\) היא **תת-קבוצה ממש** של \(B\) (או ש-\(A\) **חלקית ממש** ל-\(B\)) אם \(A \subseteq B\) וגם \(A \neq B\).

    **סימון:** \(A \subsetneq B\) או \(A \subset B\)

### משפטים חשובים

!!! abstract "משפט: קשר בין שוויון להכלה"
    $$A = B \Leftrightarrow (A \subseteq B \land B \subseteq A)$$

    זוהי הדרך הנפוצה ביותר להוכיח שוויון בין שתי קבוצות: מראים **הכלה דו-כיוונית**.

!!! abstract "משפט: טרנזיטיביות ההכלה"
    לכל שלוש קבוצות \(A, B, C\):
    $$A \subseteq B \land B \subseteq C \Rightarrow A \subseteq C$$

**הוכחה:** יהי \(x \in A\). כיוון ש-\(A \subseteq B\) נובע ש-\(x \in B\). מהעובדה ש-\(B \subseteq C\) נובע ש-\(x \in C\). ∎

!!! warning "אזהרה: הבדל בין \(\in\) ל-\(\subseteq\)"
    - **שייכות** (\(\in\)): יחס בין **איבר** לבין **קבוצה**.
    - **הכלה** (\(\subseteq\)): יחס בין **קבוצה** לבין **קבוצה**.

    לדוגמה: קבוצת המספרים הזוגיים **חלקית** לקבוצת הטבעיים, אך היא **לא שייכת** לה (כי היא עצמה אינה מספר טבעי).

---

## הקבוצה הריקה

!!! info "הגדרה: הקבוצה הריקה"
    **הקבוצה הריקה** (נסמנת \(\emptyset\) או \(\{\}\)) היא הקבוצה שאין בה איברים כלל.

    בסימון פורמלי:
    $$\forall x. x \notin \emptyset$$

!!! abstract "משפט: הקבוצה הריקה חלקית לכל קבוצה"
    לכל קבוצה \(A\) מתקיים \(\emptyset \subseteq A\).

**הוכחה:** צריך להראות ש-\(\forall x.(x \in \emptyset \rightarrow x \in A)\). מכיוון שאין איברים ב-\(\emptyset\), האגף השמאלי של הגרירה תמיד שקר, ולכן הגרירה כולה תמיד אמת. ∎

---

## אקסיומות להגדרת קבוצות

### עקרון הקומפרהנסיה המוגבל

!!! abstract "עקרון הקומפרהנסיה המוגבל"
    אם \(A\) היא קבוצה ו-\(P\) הוא תנאי (פרדיקט), אז הביטוי
    $$\{x \in A \mid P(x)\}$$
    מגדיר קבוצה. זוהי קבוצת כל האיברים מ-\(A\) שמקיימים את התנאי \(P\).

!!! example "דוגמה"
    קבוצת המספרים הזוגיים:
    $$\mathbb{N}_{\text{even}} = \{n \in \mathbb{N} \mid \exists k \in \mathbb{N}. n = 2k\}$$

### אקסיומת ההחלפה

!!! abstract "אקסיומת ההחלפה"
    אם \(F\) היא פונקציה ו-\(A\) היא קבוצה, אז הביטוי
    $$\{F(x) \mid x \in A\}$$
    מגדיר קבוצה. זוהי קבוצת כל התוצאות של הפעלת \(F\) על איברי \(A\).

!!! example "דוגמה"
    קבוצת המספרים הזוגיים (דרך נוספת):
    $$\mathbb{N}_{\text{even}} = \{2n \mid n \in \mathbb{N}\}$$

!!! note "הערה"
    שני הסימונים שקולים:
    $$\{F(x) \mid x \in A\} = \{y \in B \mid \exists x \in A. F(x) = y\}$$
    כאשר \(B\) היא קבוצה המכילה את כל הערכים האפשריים של \(F\).

---

## פעולות על קבוצות

### פעולות בסיסיות

!!! info "הגדרות: פעולות על קבוצות"
    יהיו \(A, B\) קבוצות.

    **איחוד (Union):**
    $$A \cup B = \{x \mid x \in A \lor x \in B\}$$

    **חיתוך (Intersection):**
    $$A \cap B = \{x \mid x \in A \land x \in B\}$$

    **הפרש (Difference):**
    $$A \setminus B = \{x \mid x \in A \land x \notin B\}$$

    **משלים (Complement):** ביחס לקבוצת "עולם" \(E\):
    $$\overline{A} = E \setminus A = \{x \in E \mid x \notin A\}$$

    **הפרש סימטרי (Symmetric Difference):**
    $$A \triangle B = (A \setminus B) \cup (B \setminus A)$$

### תכונות הפעולות

!!! abstract "תכונות יסודיות"
    **קומוטטיביות:**
    $$A \cap B = B \cap A \qquad A \cup B = B \cup A$$

    **אסוציאטיביות:**
    $$(A \cap B) \cap C = A \cap (B \cap C) \qquad (A \cup B) \cup C = A \cup (B \cup C)$$

    **דיסטריביוטיביות:**
    $$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$$
    $$A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$$

    **חוקי דה-מורגן:**
    $$\overline{A \cup B} = \overline{A} \cap \overline{B} \qquad \overline{A \cap B} = \overline{A} \cup \overline{B}$$

    **משלים-הפרש:**
    $$A \setminus B = A \cap \overline{B}$$

!!! example "דוגמה: הוכחת זהות בין קבוצות"
    נוכיח: \(A \setminus (B \cap C) = (A \setminus B) \cup (A \setminus C)\)

    **שיטה 1: שימוש בזהויות**
    $$A \setminus (B \cap C) = A \cap \overline{B \cap C} = A \cap (\overline{B} \cup \overline{C}) = (A \cap \overline{B}) \cup (A \cap \overline{C}) = (A \setminus B) \cup (A \setminus C)$$

    **שיטה 2: הכלה דו-כיוונית**

    **(⊆)** יהי \(x \in A \setminus (B \cap C)\). אז \(x \in A\) ו-\(x \notin B \cap C\), כלומר \(x \notin B\) או \(x \notin C\).
    - אם \(x \notin B\) אז \(x \in A \setminus B\).
    - אם \(x \notin C\) אז \(x \in A \setminus C\).

    בכל מקרה \(x \in (A \setminus B) \cup (A \setminus C)\).

    **(⊇)** יהי \(x \in (A \setminus B) \cup (A \setminus C)\).
    - אם \(x \in A \setminus B\) אז \(x \in A\) ו-\(x \notin B\), ולכן \(x \notin B \cap C\).
    - אם \(x \in A \setminus C\) אז \(x \in A\) ו-\(x \notin C\), ולכן \(x \notin B \cap C\).

    בכל מקרה \(x \in A \setminus (B \cap C)\). ∎

---

## קבוצת החזקה

!!! info "הגדרה: קבוצת החזקה"
    בהינתן קבוצה \(A\), **קבוצת החזקה** שלה, \(\mathcal{P}(A)\), מוגדרת כקבוצת כל תתי-הקבוצות של \(A\):
    $$\mathcal{P}(A) = \{B \mid B \subseteq A\}$$

!!! note "תכונה חשובה"
    לכל קבוצה \(B\) מתקיים:
    $$B \in \mathcal{P}(A) \Leftrightarrow B \subseteq A$$

!!! example "דוגמאות"
    - \(\mathcal{P}(\emptyset) = \{\emptyset\}\)
    - \(\mathcal{P}(\{1\}) = \{\emptyset, \{1\}\}\)
    - \(\mathcal{P}(\{1, 2\}) = \{\emptyset, \{1\}, \{2\}, \{1, 2\}\}\)
    - \(\mathcal{P}(\mathcal{P}(\{1\})) = \{\emptyset, \{\emptyset\}, \{\{1\}\}, \{\emptyset, \{1\}\}\}\)

!!! abstract "משפט"
    $$A \subseteq B \Leftrightarrow \mathcal{P}(A) \subseteq \mathcal{P}(B)$$

**הוכחה:**

**(→)** נניח \(A \subseteq B\). תהא \(X \in \mathcal{P}(A)\). אז \(X \subseteq A\). מטרנזיטיביות ההכלה, \(X \subseteq B\), ולכן \(X \in \mathcal{P}(B)\).

**(←)** נניח \(\mathcal{P}(A) \subseteq \mathcal{P}(B)\). יהי \(x \in A\). אז \(\{x\} \subseteq A\), ולכן \(\{x\} \in \mathcal{P}(A)\). מההנחה, \(\{x\} \in \mathcal{P}(B)\), ולכן \(\{x\} \subseteq B\), ומכאן \(x \in B\). ∎

---

## איחוד וחיתוך מוכללים

### הגדרה באמצעות קבוצה של קבוצות

!!! info "הגדרה: איחוד וחיתוך מוכללים"
    תהי \(\mathcal{F}\) קבוצה של קבוצות.

    **איחוד מוכלל:**
    $$\bigcup \mathcal{F} = \{x \mid \exists A \in \mathcal{F}. x \in A\}$$

    **חיתוך מוכלל** (מוגדר רק אם \(\mathcal{F} \neq \emptyset\)):
    $$\bigcap \mathcal{F} = \{x \mid \forall A \in \mathcal{F}. x \in A\}$$

### הגדרה באמצעות קבוצת אינדקסים

!!! info "הגדרה: סימון אינדקסים"
    תהי \(I\) קבוצת אינדקסים, ולכל \(i \in I\) תהי \(A_i\) קבוצה.

    **איחוד:**
    $$\bigcup_{i \in I} A_i = \{x \mid \exists i \in I. x \in A_i\}$$

    **חיתוך** (כאשר \(I \neq \emptyset\)):
    $$\bigcap_{i \in I} A_i = \{x \mid \forall i \in I. x \in A_i\}$$

!!! example "דוגמאות"
    עבור \(\mathcal{X} = \{\emptyset, \{\emptyset\}, \{\{\emptyset\}\}\}\):
    $$\bigcup \mathcal{X} = \{\emptyset, \{\emptyset\}\} \qquad \bigcap \mathcal{X} = \emptyset$$

    עבור קטעים:
    $$\bigcup_{x \in \mathbb{R}^+} (0, x) = \mathbb{R}^+ = (0, \infty) \qquad \bigcap_{x \in \mathbb{R}^+} (0, x) = \emptyset$$

!!! example "דוגמה מפורטת"
    נוכיח: \(\displaystyle\bigcup_{k \geq 2} \left[\frac{1}{k}, 1 - \frac{1}{k}\right] = (0, 1)\)

    **(⊆)** יהי \(x\) באיחוד. אז קיים \(k \geq 2\) כך ש-\(\frac{1}{k} \leq x \leq 1 - \frac{1}{k}\). מכיוון ש-\(k \geq 2\), מתקיים \(0 < \frac{1}{k} \leq x \leq 1 - \frac{1}{k} < 1\), ולכן \(x \in (0, 1)\).

    **(⊇)** יהי \(x \in (0, 1)\). נבחר \(k = \max\left\{\left\lceil\frac{1}{x}\right\rceil, \left\lceil\frac{1}{1-x}\right\rceil, 2\right\}\). אז \(k \geq 2\), וגם \(k \geq \frac{1}{x}\) (כלומר \(x \geq \frac{1}{k}\)) וגם \(k \geq \frac{1}{1-x}\) (כלומר \(x \leq 1 - \frac{1}{k}\)). ∎

---

## מלכודות נפוצות

!!! warning "מלכודות נפוצות"
    1. **בלבול בין \(\in\) ל-\(\subseteq\):**
       - \(1 \in \{1, 2\}\) ✓
       - \(\{1\} \subseteq \{1, 2\}\) ✓
       - \(\{1\} \in \{1, 2\}\) ✗ (אלא אם \(\{1\}\) הוא עצמו איבר)

    2. **בלבול בין \(\emptyset\) ל-\(\{\emptyset\}\):**
       - \(\emptyset\) היא הקבוצה הריקה (0 איברים)
       - \(\{\emptyset\}\) היא קבוצה עם איבר אחד (הקבוצה הריקה)

    3. **\(\in\) אינה טרנזיטיבית:**
       - אם \(A \in B\) ו-\(B \in C\), לא בהכרח \(A \in C\).
       - דוגמה נגדית: \(A = \{2\}\), \(B = \{\{2\}, 2\}\), \(C = \{\{\{2\}, 2\}\}\).

---

## תרגילים לדוגמה

!!! example "תרגיל 1"
    אילו מהטענות הבאות נכונות?

    1. \(\emptyset \in \emptyset\) — **לא נכון** (אין איברים ב-\(\emptyset\))
    2. \(\emptyset \subseteq \emptyset\) — **נכון** (הריקה חלקית לכל קבוצה)
    3. \(\emptyset \in \{\emptyset\}\) — **נכון** (הריקה היא איבר)
    4. \(\emptyset \subseteq \{\emptyset\}\) — **נכון** (הריקה חלקית לכל קבוצה)
    5. \(\{2, 3\} \subseteq \{1, 2, \{2, 3\}, 4\}\) — **לא נכון** (\(3\) לא איבר בקבוצה הימנית)
    6. \(\{2, 3\} \in \{1, 2, \{2, 3\}, 4\}\) — **נכון** (\(\{2,3\}\) הוא איבר)

!!! example "תרגיל 2"
    מצאו תנאי הכרחי ומספיק לכך ש-\(\mathcal{P}(A) \cup \mathcal{P}(B) = \mathcal{P}(A \cup B)\).

    **תשובה:** \(A \subseteq B\) או \(B \subseteq A\).

    **הוכחת המספיקות:** נניח \(A \subseteq B\). אז \(A \cup B = B\), ו-\(\mathcal{P}(A) \subseteq \mathcal{P}(B)\). לכן \(\mathcal{P}(A) \cup \mathcal{P}(B) = \mathcal{P}(B) = \mathcal{P}(A \cup B)\).

    **הוכחת ההכרחיות:** נניח ששתי הקבוצות לא מוכלות זו בזו. אז קיימים \(a \in A \setminus B\) ו-\(b \in B \setminus A\). הקבוצה \(\{a, b\}\) שייכת ל-\(\mathcal{P}(A \cup B)\) אך לא ל-\(\mathcal{P}(A)\) ולא ל-\(\mathcal{P}(B)\), ולכן לא לאיחוד שלהן.

---

## מקורות

- `discrete1-the_course_book.txt` - פרק ב.1 (מושגי יסוד), פרק ב.2 (הגדרת קבוצות וסימונן), פרק ב.3 (פעולות על קבוצות)
- `discrete1-recitations_1-13.txt` - תרגולים 2 ו-3
- `discrete_mathematics1-extended_formula_sheet.txt`
