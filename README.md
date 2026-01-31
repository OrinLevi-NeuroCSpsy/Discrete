# מתמטיקה בדידה 1 - סיכום קורס

סיכום מקיף של קורס מתמטיקה בדידה 1 באוניברסיטת תל אביב.

## צפייה באתר

האתר זמין בכתובת: https://orinlevi.github.io/Discrete1/

## תוכן

הסיכום כולל 6 יחידות:

1. לוגיקה ופסוקים
2. קבוצות
3. יחסים
4. פונקציות
5. אינדוקציה
6. עוצמות וספירה

## מבנה הפרויקט

```
discrete1_LaTex/
├── main.tex          # קובץ ראשי LaTeX
├── preamble.tex      # הגדרות מסמך וחבילות
├── macros.tex        # פקודות וסביבות מותאמות
├── units/            # יחידות הקורס (unit1.tex, unit2.tex, …)
├── docs/             # קבצי האתר (MkDocs)
│   ├── index.md
│   ├── units/
│   └── stylesheets/
├── mkdocs.yml        # הגדרות MkDocs
└── .github/workflows/deploy.yml  # GitHub Actions לפריסה
```

## פיתוח מקומי

### דרישות
- Python 3.x
- MkDocs Material
- XeLaTeX (לקימפול PDF)

### התקנה

```bash
pip install mkdocs-material
```

### הרצה מקומית

```bash
mkdocs serve
```

האתר יהיה זמין ב-`http://localhost:8000/`

## קימפול PDF

```bash
xelatex main.tex
xelatex main.tex  # פעם שנייה לעדכון תוכן עניינים
```

## רישיון

כל הזכויות שמורות © Orin Levi
