# תרגילי קבוצות

## תרגיל 1 - הוכחת שוויון קבוצות

**שאלה:** הוכיחו ש-$A \setminus (B \cap C) = (A \setminus B) \cup (A \setminus C)$

??? success "פתרון"
    נוכיח בשרשרת שקילויות:

    $$x \in A \setminus (B \cap C)$$

    $$\Leftrightarrow x \in A \land x \notin B \cap C \quad \text{(הגדרת הפרש)}$$

    $$\Leftrightarrow x \in A \land \lnot(x \in B \land x \in C) \quad \text{(הגדרת חיתוך)}$$

    $$\Leftrightarrow x \in A \land (x \notin B \lor x \notin C) \quad \text{(דה-מורגן)}$$

    $$\Leftrightarrow (x \in A \land x \notin B) \lor (x \in A \land x \notin C) \quad \text{(דיסטריביוטיביות)}$$

    $$\Leftrightarrow x \in A \setminus B \lor x \in A \setminus C \quad \text{(הגדרת הפרש)}$$

    $$\Leftrightarrow x \in (A \setminus B) \cup (A \setminus C) \quad \text{(הגדרת איחוד)}$$

---

## תרגיל 2 - תנאי הכרחי ומספיק

**שאלה:** באילו תנאים על $A, B$ מתקיים $A \cup B = A \setminus B$?

??? success "פתרון"
    **טענה:** $A \cup B = A \setminus B$ אם ורק אם $B = \emptyset$.

    **מספיקות ($\Leftarrow$):** נניח $B = \emptyset$.

    $$A \cup B = A \cup \emptyset = A = A \setminus \emptyset = A \setminus B \checkmark$$

    **הכרחיות ($\Rightarrow$):** נניח $A \cup B = A \setminus B$. נניח בשלילה ש-$B \neq \emptyset$, כלומר קיים $x \in B$.

    אז $x \in A \cup B$ (מהגדרת איחוד).

    מהשוויון: $x \in A \setminus B$, כלומר $x \in A$ ו-$x \notin B$.

    **סתירה!** לכן $B = \emptyset$.

---

## תרגיל 3 - קבוצת חזקה

**שאלה:** הוכיחו: $A \subseteq B \Leftrightarrow \mathcal{P}(A) \subseteq \mathcal{P}(B)$

??? success "פתרון"
    **כיוון ($\Rightarrow$):** נניח $A \subseteq B$. תהי $X \in \mathcal{P}(A)$.

    אז $X \subseteq A$. מהנחה וטרנזיטיביות: $X \subseteq B$.

    לכן $X \in \mathcal{P}(B)$. $\checkmark$

    **כיוון ($\Leftarrow$):** נניח $\mathcal{P}(A) \subseteq \mathcal{P}(B)$. יהי $x \in A$.

    אז $\{x\} \subseteq A$, לכן $\{x\} \in \mathcal{P}(A)$.

    מההנחה: $\{x\} \in \mathcal{P}(B)$, לכן $\{x\} \subseteq B$.

    מכאן $x \in B$. $\checkmark$

---

## תרגיל 4 - איחוד קבוצות חזקה

**שאלה:**

1. הראו שלא לכל $A, B$ מתקיים $\mathcal{P}(A) \cup \mathcal{P}(B) = \mathcal{P}(A \cup B)$.
2. מצאו תנאי הכרחי ומספיק לשוויון.

??? success "פתרון"
    **חלק 1 - דוגמה נגדית:**

    $A = \{1\}$, $B = \{2\}$.

    $$\mathcal{P}(A) \cup \mathcal{P}(B) = \{\emptyset, \{1\}\} \cup \{\emptyset, \{2\}\} = \{\emptyset, \{1\}, \{2\}\}$$

    $$\mathcal{P}(A \cup B) = \mathcal{P}(\{1,2\}) = \{\emptyset, \{1\}, \{2\}, \{1,2\}\}$$

    הקבוצות שונות! $\{1,2\}$ חסר בצד שמאל.

    ---

    **חלק 2 - תנאי:** $A \subseteq B \lor B \subseteq A$

    **מספיקות:** נניח $A \subseteq B$ (המקרה $B \subseteq A$ סימטרי).

    מתרגיל 3: $\mathcal{P}(A) \subseteq \mathcal{P}(B)$.

    לכן $\mathcal{P}(A) \cup \mathcal{P}(B) = \mathcal{P}(B)$.

    מ-$A \subseteq B$: $A \cup B = B$.

    לכן $\mathcal{P}(A \cup B) = \mathcal{P}(B) = \mathcal{P}(A) \cup \mathcal{P}(B)$. $\checkmark$

    **הכרחיות:** נניח $\lnot(A \subseteq B \lor B \subseteq A)$, כלומר $A \not\subseteq B \land B \not\subseteq A$.

    קיים $a \in A \setminus B$ וקיים $b \in B \setminus A$.

    אז $\{a, b\} \subseteq A \cup B$, לכן $\{a, b\} \in \mathcal{P}(A \cup B)$.

    אבל $\{a, b\} \not\subseteq A$ (כי $b \notin A$) ו-$\{a, b\} \not\subseteq B$ (כי $a \notin B$).

    לכן $\{a, b\} \notin \mathcal{P}(A) \cup \mathcal{P}(B)$.

    מכאן $\mathcal{P}(A \cup B) \neq \mathcal{P}(A) \cup \mathcal{P}(B)$. $\checkmark$

---

## תרגיל 5 - איחוד וחיתוך מוכללים

**שאלה:** הוכיחו ש:
$$\bigcup_{k \geq 2} \left(\frac{1}{k}, 1 - \frac{1}{k}\right) = (0, 1)$$

??? success "פתרון"
    **הכלה $\subseteq$:** יהי $x \in \bigcup_{k \geq 2} \left(\frac{1}{k}, 1 - \frac{1}{k}\right)$.

    קיים $k \geq 2$ כך ש-$x \in \left(\frac{1}{k}, 1 - \frac{1}{k}\right)$.

    לכן $\frac{1}{k} < x < 1 - \frac{1}{k}$.

    מ-$k \geq 2$: $\frac{1}{k} \leq \frac{1}{2} < 1$ ו-$1 - \frac{1}{k} \geq \frac{1}{2} > 0$.

    לכן $0 < x < 1$, כלומר $x \in (0, 1)$. $\checkmark$

    ---

    **הכלה $\supseteq$:** יהי $x \in (0, 1)$.

    צ"ל: קיים $k \geq 2$ כך ש-$\frac{1}{k} < x < 1 - \frac{1}{k}$.

    ניקח $k$ גדול מספיק כך ש-$\frac{1}{k} < \min(x, 1-x)$.

    (זה אפשרי כי $x > 0$ ו-$1-x > 0$.)

    אז $\frac{1}{k} < x$ וגם $\frac{1}{k} < 1-x$, כלומר $x < 1 - \frac{1}{k}$.

    לכן $x \in \left(\frac{1}{k}, 1 - \frac{1}{k}\right) \subseteq \bigcup_{k \geq 2} \left(\frac{1}{k}, 1 - \frac{1}{k}\right)$. $\checkmark$

---

## תרגיל 6 - חיתוך מוכלל

**שאלה:** חשבו את $\bigcap_{x \in \mathbb{R}^+} (0, x)$.

??? success "פתרון"
    **טענה:** $\bigcap_{x \in \mathbb{R}^+} (0, x) = \emptyset$

    **הוכחה:** נניח בשלילה שקיים $y \in \bigcap_{x \in \mathbb{R}^+} (0, x)$.

    אז לכל $x \in \mathbb{R}^+$: $y \in (0, x)$, כלומר $0 < y < x$.

    בפרט, עבור $x = \frac{y}{2}$ (שהוא חיובי כי $y > 0$):

    $y < \frac{y}{2}$ - **סתירה!**

    לכן $\bigcap_{x \in \mathbb{R}^+} (0, x) = \emptyset$.

---

## טבלת זהויות חשובות

| זהות | שם |
|------|----|
| $A \cup \emptyset = A$ | איחוד עם ריקה |
| $A \cap \emptyset = \emptyset$ | חיתוך עם ריקה |
| $A \setminus A = \emptyset$ | הפרש עצמי |
| $A \setminus \emptyset = A$ | הפרש מריקה |
| $\overline{A \cup B} = \overline{A} \cap \overline{B}$ | דה-מורגן |
| $\overline{A \cap B} = \overline{A} \cup \overline{B}$ | דה-מורגן |
| $A \setminus (B \cap C) = (A \setminus B) \cup (A \setminus C)$ | דיסטריביוטיביות |
| $A \setminus (B \cup C) = (A \setminus B) \cap (A \setminus C)$ | דיסטריביוטיביות |

---

## טיפים

!!! tip "טיפים לתרגילי קבוצות"
    1. **הוכחת שוויון:** הראו הכלה דו-כיוונית $\subseteq$ ו-$\supseteq$
    2. **הפרכה:** מספיקה דוגמה נגדית פשוטה (קבוצות קטנות!)
    3. **תנאי הכרחי ומספיק:** צריך להוכיח שני כיוונים
    4. **קבוצת חזקה:** זכרו $X \in \mathcal{P}(A) \Leftrightarrow X \subseteq A$
    5. **פעולות מוכללות:** כתבו את ההגדרה ועבדו איתה
