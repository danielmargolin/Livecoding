# Fylo שדרוג קוד

<div dir="rtl">
<p> בחרתי לעבוד עם בייטים (במקום מגה בייט).
למה?
תסתכלו על הקוד שכתבנו בכיתה.. מה יקרה אם נחליט לשנות ל2000 מגה? בעיה.
הקוד לא מספיק גמיש.
שימו לב: ההמרה לפורמט ״יפה״ (מגה,גיג׳ה וכו׳) תיקרה רק לפני הכתיבה למסך (לפני כן נוח לנו לעבוד עם בייטים כי גם file.size מיוצג בבייטים)
</p>
<h2>
הסבר על כל פונקציה:
</h2>
<h3>
initApp - אחראית על איתחול האפליקציה
</h3>
<ul>
<li>
פונקציה שלא מקבלת פרמטרים
</li>
<li>
 קוראת מהלוקל סטורג׳
</li>
<li>
 קוראת לupdateDashboard עם הפרמטר usedSizeInBytes
</li>
</ul>
<h3>
updateDashboard - מקבלת את מספר הבייטים בשימוש ואחראית על עידכון המסך
</h3>
<ul>
<li>
 תקרא ל updateSizes כדי לעדכן את המספרים במסך
</li>
<li>
 תעדכן את שאר הדברים (כמו הפרוגרס בר)
</li>
</ul>
<h3>
updateSizes - פונקציה שתעדכן את המספרים והיחידות מידה במסך
</h3>
<ul>
<li>
 מקבלת גודל בבייטים ואת האלמנטים שצריך לעדכן
</li>
<li>
 סתם כתבתי אותה כי ראיתי שיש הרבה קוד שחוזר על עצמו, אז העדפתי לקרוא לה כמה פעמים עם הפרמטרים הרלוונטיים
</li>
<li>
 תעזר ב getFormattedBytes בשביל לקבל ייצוג יפה של הגודל
</li>
</ul>
<h3>
getFormattedBytes - מקבלת מספר בייטים ומחזירה אותם בצורה יפה יותר (מגה בייט, גיג׳ה בייט וכו׳)
</h3>
<ul>
<li>
• סתם מצאתי אותה באינטרנט :)
</li>
<li>
• מחזירה אובייקט עם שני מפתחות: גודל ויחידת מידה (למשל, גודל: 25, יחידת מידה: מגה)
</li>
</ul>
<h3>
onFileInputChange - אחראית לבדוק אם הקובץ הוא תמונה
</h3>
<ul>
<li>
 תרוץ כשהמשתמש יבחר קובץ
</li>
<li>
 אם הקובץ תמונה, תעביר אותו ל updateFile
</li>
</ul>
<h3>
updateFile - מקבלת קובץ ואחראית על לעדכן משתנים (ולוקל סטורג׳)
</h3>
<ul>
<li>
• כשיהיה לנו שרת, יכול להיות שהפונקציה הזו תדאג להעלאת הקובץ
</li>
<li>
• היחידה שמעדכנת את הלוקל סטורג׳
</li>
</ul>

<h3>
הערות:
</h3>
הייתי צריך לשנות טיפה את הhtml - תיראו בpr
אחרי בדיקה, הייתה לי טעות קטנה. הפרמטר שמקבלים בשימוש addEventListener הוא אכן event.
ואילו כאשר ניגשים מהhtml אל הjs ומעבירים את this, נקבל את האלמנט כפרמטר (ראו בקובץ html).
אם נכתוב בhtml:
onchange="onFileInputChange(event)"
נקבל את event (כמו בשימוש ב addEventListener)
שימו לב שהוספתי תיקון לבאג שכנראה יש לכולכם: onclick שהעברתי לfile input הוא כדי שיהיה אפשר לבחור את אותו הקובץ פעמיים ברצף.
קישור לבעיה + פתרון:
https://stackoverflow.com/questions/4109276/how-to-detect-input-type-file-change-for-the-same-file
שימו לב שאנחנו קוראים מהלוקל סטורג׳ רק פעם אחת (בניגוד לפתרון שראינו בסשן)
תרגישו חופשי להשתמש בקוד או אולי אפילו לשפר אותו :)

## </div>

### Table of Contents

- [Challenge Languages](#Languages)
- [Instructions](#Instructions)
- [Style Guide](#Style-Guide)
- [Preview](#Preview)

---

## Languages

- HTML
- CSS

---

## Instructions

- [ ] Clone this repository.
- [ ] Checkout to the starting-files branch
- [ ] Try to mimic the site listed bellow.
- [ ] (optional) mimic the mobile design as well for mobile users.

---

## STYLE GUIDE:

Please fill free to use this style guide to complete the task.

### Colors:

    Progress bar gradient = hsl(6, 100%, 80%) to hsl(335, 100%, 65%)
    Site background = hsl(229, 57%, 11%)
    Floating sections = hsl(228, 56%, 26%)
    Text 1 color = hsl(229, 7%, 55%)
    Text 2 color = white
    Icon color = hsl(243, 100%, 93%)

### Fonts (google font):

    main = 'Raleway' , 22.4px , regular
    headline = 'Raleway' , 48px , bold

### Positions:

    Row Width = 80%
    Col Gap = 32px;

---

## Preview

![!preview](./design/desktop-design.jpg)

**GOOD LUCK!**🚀
