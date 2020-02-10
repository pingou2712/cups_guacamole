Fork of cups-pdf
Sorry for my english (i'm french)

It's for printer with guacamole (linux desktop)

Printer native of guacamole don't work with me.... (it's really work for someone? on linux desktop?)
So i use cups-pdf to print directly on Download directory of guacamole
(Don't need printer enabled of user-mapping.mxl, just need enable-drive)
But there are error because the tests to create directory thinclient... change owner etc etc... normal

So only change at the moment:

*It's not a good job but it's work (not time for moment):
Change return 1 to return 0
line:122 and 523

*And changement name and necessary for that...


To install:

("apt source cups" and "cups devel" needed)
gcc -O9 -s cups-guacamole.c -o /usr/lib/cups/backend/cups-guacamole -lcups

mkdir /usr/share/ppd/cups-guacamole
cp CUPS-GUACAMOLE_opt.ppd /usr/share/ppd/cups-guacamole/CUPS-GUACAMOLE_opt.ppd

cp cups-guacamole.conf /etc/cups/cups-guacamole.conf
change directory on cups-guacamole.conf if needed

And add printer via cups!! 
enjoy 
Vincent L.

Note:
You can use : PostProcessing line in config but:
-> need 2 congfig file for cup if you need a "normal" pdfprinter and i don't know do that simply...
-> print write first in pdf directory and after move it in Guacfs directory so 2 write for 1...
