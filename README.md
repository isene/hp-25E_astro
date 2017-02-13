# hp-25E_astro
Turning the HP-25E into the ultimate amateur astronomy calculator.

The HP-25E is an original HP-25 with a brain transplant.

Berhard Emese has created a wonderful upgrade to the HP Woodstock calculator series (the HP-21 - HP-29C) as well as other old HP calculators. His HP-25E is a wonderful device capable of far more than the original HP-25. See his page for details: http://www.panamatik.de/html/hp_calculator_repair_kit.html

This ASTRO program makes extensive use of the dynamic program loading. The program file name indicates where the program is to be stored (the main program, HP-25_ASTRO-60-MAIN.25, is stored in program storage #60, while HP-25_ASTRO-61-JD1.25 is stored in #61, etc.)

To start these programs, first go to the GPS module (g STO), wait for the GPS to start the time running and do a continual storage of the time in register 0 (f STO 0). Then go to the Latitude and store the number in register 6 (STO 6). Finally store the Longitude in register 7 (STO 7). Go back to RUN mode, make sure you have the main program loaded (HP-25_ASTRO-60-MAIN.25), store your time zone in register 1 (e.g. 1 for UTC+1, STO 1). Then enter the current date (YYYY.MMDD) and press R/S.

The program spits out the current local time. Pressing R/S again gives you the new time, etc.

If you enter the number 1 and then press R/S, the program jumps to "module 1" (calculate Julian Day, JD) and spits out the JD. Pressing R/S brings you back to the main program and it gives you the current local time again.
