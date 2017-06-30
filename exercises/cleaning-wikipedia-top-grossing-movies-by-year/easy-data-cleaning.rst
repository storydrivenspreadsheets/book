

Step 0: Copy and paste
======================


https://en.wikipedia.org/wiki/List_of_highest-grossing_films#High-grossing_films_by_year

Actual:

https://en.wikipedia.org/w/index.php?title=List_of_highest-grossing_films&oldid=788016578


Spreadsheet:

https://docs.google.com/spreadsheets/d/1nTjnWUpBx69RqCqEFrIhiEFCVmrzKiDbZt_wtHf_a1o/edit#gid=0


Step 1: Paste as values
=======================

https://docs.google.com/spreadsheets/d/1nTjnWUpBx69RqCqEFrIhiEFCVmrzKiDbZt_wtHf_a1o/edit#gid=1440002071

Step 2: Quality of life fixes
=============================

https://docs.google.com/spreadsheets/d/1nTjnWUpBx69RqCqEFrIhiEFCVmrzKiDbZt_wtHf_a1o/edit#gid=1978041151

- Delete "References"
- Fit cell to data
- Bold headers
- Freeze header row
- Top align





Step 3: Year fill down
======================

https://docs.google.com/spreadsheets/d/1nTjnWUpBx69RqCqEFrIhiEFCVmrzKiDbZt_wtHf_a1o/edit#gid=482589241

```
  =IF(ISBLANK(A2), INDIRECT(ADDRESS(ROW()-1,COLUMN()), A2))
```


Step 4: Create plaingross and plainbudget
=========================================

WTF is Towering Inferno
https://en.wikipedia.org/wiki/The_Towering_Inferno



https://docs.google.com/spreadsheets/d/1nTjnWUpBx69RqCqEFrIhiEFCVmrzKiDbZt_wtHf_a1o/edit#gid=33178265

- Watch out for that mdash: `–`
- Have to account for some columns being numbers
- REGEX removes unneded characters
- Make opinionated decision that we only care about lows and highs
=REGEXREPLACE(TO_TEXT(C2), "[^\d–\s\(\)/]", "")
=REGEXREPLACE(TO_TEXT(D2), "[^\d–\s\(\)/]", "")

Capture only the top line value

=IF(REGEXMATCH(TO_TEXT(C2), "\n"), REGEXEXTRACT(TO_TEXT(C2), "^.+\n"), TO_TEXT(C2))

strip out anything inside parentheses

=REGEXREPLACE(
  IF(REGEXMATCH(TO_TEXT(C2), "\n"), REGEXEXTRACT(TO_TEXT(C2), "^.+\n"), TO_TEXT(C2)),
  "\(.+?\)", ""
)

Delete all non-numerical, non-mdash values

=REGEXREPLACE(
  REGEXREPLACE(
    IF(REGEXMATCH(TO_TEXT(C2), "\n"), REGEXEXTRACT(TO_TEXT(C2), "^.+\n"), TO_TEXT(C2)),
    "\(.+?\)", ""
  ),
  "[^\d–]", ""
)

Alternatively:

```
=IF(NOT(ISTEXT(D2)),
   TO_TEXT(D2),
   REGEXREPLACE(
     REGEXREPLACE(
       IF(REGEXMATCH(D2, "\n"),
         REGEXEXTRACT(D2, "^.+?\n"),
         D2
       ),
       "\(.+?\)",
       ""
     ),
     "[^\d–./]",
     ""
  )
)
```



Same for plain budget

```
=IF(NOT(ISTEXT(F2)),
   TO_TEXT(F2),
   REGEXREPLACE(
     REGEXREPLACE(
       IF(REGEXMATCH(F2, "\n"),
         REGEXEXTRACT(F2, "^.+?\n"),
         F2
       ),
       "\(.+?\)",
       ""
     ),
     "[^\d–./]",
     ""
  )
)
```




Step 5: Create low-high ranges
==============================

=TO_PURE_NUMBER(REGEXEXTRACT(E2, "^\d+"))
=TO_PURE_NUMBER(REGEXEXTRACT(E2, "^\d+"))
=ROUND((F2 + G2)/2)
