# hp-25E_astro
Turning the HP-25E into the ultimate amateur astronomy calculator.

The HP-25E is an original HP-25 with a brain transplant.

Berhard Emese has created a wonderful upgrade to the HP Woodstock calculator series (the HP-21 - HP-29C) as well as other old HP calculators. His HP-25E is a wonderful device capable of far more than the original HP-25. See his page for details: http://www.panamatik.de/html/hp_calculator_repair_kit.html

This ASTRO program makes extensive use of the dynamic program loading. The program file name indicates where the program is to be stored (the main program, HP-25_ASTRO-60-MAIN.25, is stored in program storage #60, while HP-25_ASTRO-61-JD1.25 is stored in #61, etc.)

To start these programs, first go to the GPS module (g STO), wait for the GPS to start the time running and do a continual storage of the time in register 0 (f STO 0). Then go to the Latitude and store the number in register 6 (STO 6). Finally store the Longitude in register 7 (STO 7). Go back to RUN mode, make sure you have the main program loaded (HP-25_ASTRO-60-MAIN.25), store your time zone in register 1 (e.g. 1 for UTC+1, STO 1). Then enter the current date (YYYY.MMDD) and press R/S. YYYY is stored in Register 3, MM in Reg 4 and DD in Reg 5.

The program spits out the current local time. Pressing R/S again gives you the new time, etc.

If you enter the number 1 and then press R/S, the program jumps to "module 1" (calculate Julian Day, JD) and spits out the JD. Pressing R/S brings you back to the main program and it gives you the current local time again.

The following program modules are available (pressing the module number and R/S after the time is displayed will launch the module as explained above):

* 1: With YYYY in Reg 3, MM in Reg 4 and DD in Reg 5 (and time in Reg 0), pressing 1 and R/S displays the Julian Date (JD) with integer part in X and fractional part in Y (to avoid rounding problems with the accuracy of seconds). Pressing R/S gets you back to the main program (#60) with the current time displayed and with JD (integer) in Reg Y and JD (fractional) in Reg Z.
* 2: With the integer part of JD in X and fractional part in Y, pressing 2 and R/S will return YYYY.MMDD in X and HH.mmss in Y. It leaves YYYY in Reg 3, MM in Reg 4 and DD in Reg 5. Pressing R/S brings you back to the main program (#60) with the current time in X, YYYY.MMDD from the JD in Y and HH.mmss from the JD is left in the Z register.

(more modules to come)

In the program listings, the checksum is shown in parentheses behind the last program step in each page.

I have also made a VIM filetype and syntax plugin to facilitate the creation of HP-25 programs (using ".25" as file extension): https://github.com/isene/hp-25_vim

### License
This software is released into the Public Domain.
