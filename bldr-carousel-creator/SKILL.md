---
name: bldr-carousel-creator
description: "יוצר קרוסלות לאינסטגרם בסגנון BLDR. משתמש בשפת המותג המלאה עם פונטי FbAbsoluti, גרדיאנטים, grain texture וחלונות דפדפן אפל. תומך בשקפי טקסט, תמונות, terminal ו-CTA. השתמש בסקיל הזה בכל פעם שערן מבקש לבנות קרוסלה, לעצב שקפים לאינסטגרם, ליצור תוכן ויזואלי לפוסטים, או כשהוא אומר תעשה קרוסלה, תבנה שקפים, קרוסלת אינסטגרם."
---

# BLDR Carousel Creator

יצירת קרוסלות לאינסטגרם בפורמט 4:5 (1080x1350) בסגנון BLDR Agentic World.

## כללים קבועים

- פורמט: 4:5 תמיד. Preview ב-270x338px
- פונטים: FbAbsoluti Black (900) לכותרות. FbAbsoluti Light (300) לגוף.
  - https://raw.githubusercontent.com/Baranesyea/Eransfonts/main/FbAbsolutiHeb-Black.woff2
    - https://raw.githubusercontent.com/Baranesyea/Eransfonts/main/FbAbsolutiHeb-Light.woff2
    - רקע: תמיד #050510
    - כיוון: תמיד RTL
    - אסור: אימוג'י, מקפים, דשים. במקום דשים: פסיק או נקודה
    - אסור: מילה אוטומציה. תמיד: סוכנים או תהליכי עבודה אג'נטיים
    - פנייה: תמיד בגוף רבים (אתם/לכם)

    ## שכבות שקף

    Layer 1 (z:1) grain texture
    Layer 2 (z:2) blue glow radial-gradient מפינה ימנית עליונה rgba(51,51,255,0.22)
    Layer 3 (z:3) content טקסט ותמונות
    Layer 4 (z:4) corner overlay גרדיאנט כהה מעל הטקסט בפינה ימנית עליונה
    Layer 5 (z:5) bottom bar progress + meta
    Layer 6 (z:6) save hint שקף 1 בלבד

    ## טיפוגרפיה

    שורה קטנה מעל כותרת: FbAbsoluti, 11-13px, weight 900, #fff
    כותרת גדולה: FbAbsoluti, 30-36px, weight 900, #fff
    נקודה בסוף כותרת: #0000FF
    קו accent: 22-28px רוחב, 2px גובה, #0000FF עם glow
    טקסט גוף: FbAbsoluti, 11-14px, weight 300, #fff
    bullet dot: 5x5px עגול, #0000FF עם glow
    brand BLDR: FbAbsoluti, 9px, weight 900, rgba(240,240,245,0.22)
    מונה שקפים: FbAbsoluti, 9px, weight 300, rgba(240,240,245,0.2)

    ## פלטת צבעים

    BG: #050510
    Surface: #0a0a1a
    Primary: #0000FF
    Glow: rgba(51,51,255,0.22)
    Text: #fff
    Text muted: rgba(240,240,245,0.22)
    Border: rgba(255,255,255,0.08)

    ## בר תחתון

    קו רציף שמתמלא. fill width = ((cur+1) / TOTAL * 100)%
    track: height 2px, background rgba(255,255,255,0.15)
    fill: background rgba(255,255,255,0.88), transition width 0.35s cubic-bezier(.4,0,.2,1)

    ## חלון דפדפן אפל

    3 נקודות: red #ff5f57, yellow #febc2e, green #28c840
    url bar: bg #2c2c2e, font-size 7px, monospace
    browser body: terminal lines עם prompt ($), command, thinking, tasks, output
    glow: box-shadow 0 0 14px rgba(0,0,255,0.15)

    ## סוגי שקפים

    Cover: שורה קטנה + כותרת + acc line + טקסט גוף + כפתור שמירה בפינה שמאלית תחתונה z:6
    Body: שורה קטנה + כותרת + acc line + טקסט גוף
    Bullets: שורה קטנה + כותרת + acc line + רשימה עם נקודות כחולות
    Browser: שורה קטנה + כותרת + acc line + טקסט קצר + חלון דפדפן
    CTA: שורה קטנה + כותרת + acc line + טקסט גוף + כפתור כחול Agentic World

    ## כפתור שמירה שקף 1

    position absolute, bottom 36px, left 14px, z-index 6
    bookmark SVG icon, stroke rgba(255,255,255,0.7), 12px
    טקסט: FbAbsoluti, 8px, weight 300, rgba(255,255,255,0.5), לשמור לאחר כך

    ## תמונות

    border-radius: 6-8px
    box-shadow: 0 0 12px rgba(0,0,255,0.18)

    ## ניווט

    לחיצה על חצי שמאלי של השקף = קדימה
    לחיצה על חצי ימני של השקף = אחורה
    כפתורי nav מחוץ לשקף עם חצים

    ## תהליך עבודה

    1. שאל על: מספר שקפים, נושא, האם יש תמונות
    2. הגדר מבנה שקפים
    3. בנה widget עם הפונטים מ-GitHub
    4. הצג preview אינטראקטיבי
    5. תקן לפי פידבק
