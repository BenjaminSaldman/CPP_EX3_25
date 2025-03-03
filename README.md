<div dir="rtl" lang="he">

# מטלה מספר 3 - קו - מחלקות וירושה

קו (coup - הפיכה) הוא משחק קופסה עבור 2-6 שחקנים המשחקים אחד נגד השני כדי להישאר אחרונים על המגרש.

במטלה זו נממש חלק מחוקי המשחק.

## חוקי המשחק
בתחילת המשחק כל שחקן שולף קלף מהערימה. כל קלף מתאר  תפקיד אותו יכול לממש השחקן.  במרכז השולחן ישנה קופה של מטבעות. כל שחקן בתורו משחק לפי התפקיד אליו משתייך (פירוט התפקידים בהמשך) ויכול לקחת מטבעות בהתאם. מטרת המשחק היא להוציא לפועל "הפיכות" ולהדיח שחקנים אחרים מתפקידם. השחקן האחרון שנשאר בעל תפקיד מנצח.
 
## השחקן

לכל שחקן יש שם משלו. 

בכל תור יכול שחקן, בלי קשר לתפקידו, לבצע את אחת מהפעולות הבאות:

1. שכר - `income` - לקחת מטבע מהערימה.  
לפעולה זו אין עלות, אין פעולות נגדיות והשחקן מרוויח מטבע בודד.

2. שכר כפול - `foreign_aid` - לקחת שני מטבעות מהערימה.  
לפעולה זו אין עלות והיא מזכה את השחקן בשני מטבעות. אבל, ישנו תפקיד במשחק היכול לחסום את הפעולה הזו. אם השחקן נחסם בעת שמנסה לקחת שכר כפול, תורו מסתיים.

3. הפיכה - `coup` -  להדיח שחקן יריב מתפקידו ובכך להוציא אותו מהמשחק.  
עלות פעולה זו 7 מטבעות, אין לה פעולות נגדיות והיא מסתיימת בכך שהשחקן עליו הופעלה הפעולה מודח מתפקידו ומסיים את המשחק.

כל פעולה צריכה לעדכן את מספר המטבעות אותם מחזיק השחקן בהתאם.  
אם הפעולה לא חוקית, יש לזרוק חריגה מתאימה.

בנוסף, יש לממש את השיטות הבאות:

*  `role` - פונקציה המחזירה את התפקיד של השחקן (ראו רשימת התפקידים למטה), לצורך תצוגה.

* `coins` השיטה מחזירה כמה מטבעות יש לשחקן


## תפקידים

ישנם תפקידים שונים של שחקנים, שיש להם כישורים מיוחדים:

1. דוקס - `Duke`: יכול לקחת מס בגובה שלושה מטבעות מהקופה מבלי שאף שחקן יכול למנוע ממנו. בנוסף, הדוקס יכול לחסום פעולת שכר כפול. השחקן שנחסם מחזיר את שני המטבעות לקופה.

2. מתנקש - `Assassin`: יכול להדיח שחקן מתפקידו בעלות 3 מטבעות בלבד (במקום 7). אולם, יש תפקיד היכול למנוע פעולה זו מהמתנקש. אם מתנקש נחסם השחקן שהודח בעקבות ההתנקשות חוזר למשחק.

3. שגריר - `Ambassador`: יכול להעביר מטבע משחקן אחד לשחקן אחר בנוסף, השגריר יכול למנוע את פעולת הגניבה המפורטת בהמשך.

4. קפטן - `Captain`: יכול לגנוב 2 מטבעות משחקן אחר. פעולה זו יכולה להיחסם ע"י שגריר או ע"י קפטן אחר. (ז"א גם קפטן יכול לחסום גניבה, בדומה לשגריר).

5. רוזנת - `Contessa`: יכולה לחסום את פעולת ההתנקשות.

6. בירוקרט - `Bureaucrat`: יכול לקחת מס של 3 מטבעות ולהביא את אחד מהם לשחקן אחר. בנוסף, הוא יכול לחסום פעולת שכר כפול.


הערות:

* יכולים להיות שני שחקנים או יותר בעלי אותו תפקיד - לא קורה שום דבר מיוחד במצב זה.

* אם שחקן מחזיק 10 מטבעות בתחילת תורו, הוא חייב לבצע הפיכה באותו תור

* פעולות חסימה לא צריכות להמתין לתור השחקן החוסם ולא מבזבזות לו תור אלא מתבצעות "בזמן אמת". במשחק שלנו לא נממש תגובות "בזמן אמת" לכן ממשו את הפתרון הבא:  
שחקן שביצע פעולה שניתנת לחסימה, ניתן לחסום את הפעולה שלו עד שהגיע תורו לשחק שוב.  
דוגמה:  
שחקן 1 לקח שכר כפול ושחקן 3 מחזיק בקלף דוקס. שחקן 3 לא צריך לחכות לתורו כדי לחסום את שחקן 1. אבל, אם הגיע שוב תורו של שחקן 1, שחקן 3 כבר לא יכול לבקש ממנו להחזיר את המטבעות לקופה.

## מהלך המשחק

לכל משחק יש את השחקנים שמשחקים בו, מה מצבו של כל שחקן ובסיום המשחק, מי המנצח. בנוסף, המשחק יודע תור מי עכשיו. התורות נקבעים לפי סדר ההצטרפות למשחק.

יש לממש את השיטות

1. תור - `turn` - הדפסת שם השחקן אשר תורו לשחק כעת.
2. שחקנים פעילים - `players` - השיטה מחזירה את שמות השחקנים שפעילים כעת במשחק.
3. מנצח - `winner` - השיטה מחזירה את שם המנצח. אם המשחק עדיין פעיל, השיטה תזרוק שגיאה.


**חלק א**: יש לכתוב: 

* קובץ כותרת הכולל את כל הפונקציות הדרושות (ללא מימוש). שימו לב: הכותרות צריכות להיות נכונות בהתאם למה שנלמד בהרצאות - מומלץ לחזור על החומר לפני שמתחילים לכתוב.
* בדיקות מקיפות לכל הפונקציות הדרושות.
   * אין צורך לבדוק את  אופרטור הפלט - כיוון שלא הגדרנו את הפורמט.
  
כיתבו את כל הקבצים הדרושים כך שהפקודות הבאות יעבדו ללא שגיאות:

<div dir='ltr'>

    make demo1 && ./demo1
    make demo2 && ./demo2
	make test && ./test

</div>

מומלץ גם להריץ:

<div dir='ltr'>

    make tidy
    make valgrind

</div>

אין לשנות קבצים קיימים אלא רק להוסיף קבצים חדשים.

בהצלחה
</div>
