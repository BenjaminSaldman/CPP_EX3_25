<div dir="rtl">

# מטלה מספר 3 - קו - מחלקות וירושה

* מטרת המטלה: הבנת והטמעת העקרונות של מחלקות, עצמים וירושה.
* **שימו לב!** במטלה זו **מותר** להשתמש במבני נתונים של הספרייה הסטנדרטית.
* ההגשה ביחידים.

---

## הוראות הגשה:

ב-Moodle יש להגיש קובץ טקסט המורכב מ-3 שורות:
- בשורה הראשונה – מספר תעודת הזהות שלכם.
- בשורה השנייה – הקישור להגשה.
- בשורה השלישית – הקומיט האחרון של הפרויקט.

---

במטלה זו תייצגו את המשחק "קו" (Coup) באמצעות מחלקות וירושה. המשחק מיועד למספר שחקנים, כאשר כל שחקן מקבל תפקיד ייחודי בעל יכולות מיוחדות.

## חוקי המשחק

לכל שחקן תור לבצע פעולה אחת מבין הבאות:
- איסוף משאבים (`gather`) – קבלת מטבע אחד מהקופה, ללא עלות.
- מס (`tax`) – קבלת שני מטבעות מהקופה.
- שוחד (bribe) – שחקן משלם 4 מטבעות לשחקן אחר.
- איסוף בכוח (coup) – מחייב 7 מטבעות, מסיר שחקן מהמשחק.
- פעולות מיוחדות נוספות לפי תפקידים ספציפיים.

כל פעולה חייבת לעדכן את מצב המטבעות של השחקנים. אם פעולה לא חוקית, יש לזרוק חריגה מתאימה.

### תפקידים ויכולות מיוחדות

- **נציב (Governor)** - יכול לקחת 3 מטבעות בפעולת מס ולחסום מס של אחרים.
- **מרגל (Spy)** - יכול להציץ בקלפי התפקיד של שחקן אחר.
- **ברון (Baron)** - יכול לקבל רווח של 5 מטבעות תמורת השקעה של 3 מטבעות.
- **גנרל (General)** - פעולות התקפה שלו עולות פחות מטבע אחד.
- **שופט (Judge)** - יכול לחסום פעולה של שוחד של שחקנים אחרים.
- **סוחר (Merchant)** - יכול להרוויח מטבע נוסף כאשר לוקח מטבעות מהקופה.

## דרישות מימוש:
- ממשו מחלקה בסיסית של שחקן, ומחלקות יורשות לכל תפקיד ייחודי.
- ממשו את הפעולות הנדרשות (ראו לעיל).
- יש לבדוק את תקינות הקלט ולזרוק חריגות (exceptions) במידת הצורך.

## מהלך המשחק


המשחק צריך לתמוך בממשק הבא:
 `turn` - מחזירה את שם השחקן שתורו כעת.
 `players` - מחזירה את רשימת השחקנים הפעילים במשחק.
 `winner` - מחזירה את שם השחקן המנצח.

---

### דרישות טכניות:
- יש לכתוב בדיקות יחידה (unit tests) לכל הפונקציות.
- יש לכתוב קובץ `main` להדגמת המשחק וקובץ `Makefile` הכולל:
  - פקודה `make Main` להרצת ההדגמה.
  - פקודה `make test` להרצת בדיקות היחידה.

- יש לבדוק שאין זליגת זיכרון באמצעות `valgrind`.

---

### הנחיות הגשה נוספות:
- בתחילת **כל** קובץ יש לרשום את כתובת המייל שלכם.
- הגישו קובץ `README` המתאר את ההיררכיה של המחלקות ואת הספריות שהשתמשתם בהן.
- חובה לדווח בכתב על כל עזרה שקיבלתם, בהתאם ל[תקנון היושר של המחלקה](https://www.ariel.ac.il/wp/cs/wp-content/uploads/sites/88/2020/08/Guidelines-for-Academic-Integrity.pdf).

מותר להתייעץ עם סטודנטים אחרים או לחפש מידע באינטרנט; אסור להעתיק קטעי-קוד שלמים מסטודנטים אחרים, מהאינטרנט וממודלי בינה מלאכותית (למשל, chatGPT).

בהצלחה!

</div>

