# Discrete Mathematics 1 — LaTeX Notes

תרגום ועיבוד של סיכומי הקורס מתמטיקה בדידה 1 (אוניברסיטת תל אביב).

## מבנה הפרויקט

- `main.tex` — קובץ ראשי, טבלת תוכן וכל היחידות
- `preamble.tex` — הגדרות מסמך וחבילות
- `macros.tex` — פקודות וסביבות מותאמות
- `units/` — יחידות הקורס (unit1.tex, unit2.tex, …)

## בניית ה-PDF

דרושות התקנת TeX (למשל [TeX Live](https://www.tug.org/texlive/) או [MiKTeX](https://miktex.org/)).

```bash
xelatex main.tex
```

למסמך עם טבלת תוכן מעודכנת הרץ פעמיים:

```bash
xelatex main.tex
xelatex main.tex
```

## מחבר

Orin Levi
