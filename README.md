Sorry for my english (i'm french)

Fork of cups-pdf

Printer of guacamole don't work with me....
So i use cups-pdf to print directly on Download directory of guacamole
(Don't need printer enabled of user-mapping.mxl, just need enable-drive)
But error because test to create thinclient...

So only change at the moment:

*It's not a good job but it's work (not time for moment)
Change return 1 to return 0
line:122 and 522

*And changement name and necessary for that...


To install:

gcc -O9 -s cups-pdf.c -o /usr/lib/cups/backend/cups-guacamole -lcups

mkdir /usr/share/ppd/cups-guacamole
cp CUPS-GUACAMOLE_opt.ppd /usr/share/ppd/cups-guacamole/CUPS-GUACAMOLE_opt.ppd

cp cups-guacamole.conf /etc/cups/cups-guacamole.conf
change directory on cups-guacamole.conf if needed

And add printer via cups!! 
enjoy
