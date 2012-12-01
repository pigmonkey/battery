battery
=======

I run my electronics on [Sanyo Eneloop](http://www.eneloop.info/) rechargeable
batteries. The batteries are charged with a [PowerEx
MH-C9000](http://www.amazon.com/gp/product/B000NLUSLM) charger.

`batteries.csv` is a database of my batteries. Each battery is labeled, and I
track the date I purchased the battery, the current capacity, the date on which
the battery was last charged, and the date on which the battery was last ran
through the MH-C9000's refresh and analyze (R/A) mode. Tracking this
information in git allows me to build up a historical record of an individual
battery's performance.

The database is a tab-delimited CSV file. Fields are separated by multiple tabs
so that the file is more pleasant to view in a [text
editor](http://www.vim.org/). If a [graphical spreadsheet
program](https://www.libreoffice.org/features/calc/) is used, the program
should be told to merge delimiters for viewing. The file can be also be simply
viewed on the command-line.

    $ column -t batteries.csv | less -NS -#2


Charge / Discharge Rates
------------------------

Eneloop AA batteries have a listed capacity (C) of 2000 mAh. Eneloop AAA
batteries have a listed capacity (C) of 800 mAh.

Maha / PowerEx recommends charging batteries at 0.5C and discharging at 0.25C.
I've stuck with these rates so far.

### AA

Charge:     1000 mA Discharge:  500 mA

### AAA

Charge:     400 mA Discharge:  200 mA
