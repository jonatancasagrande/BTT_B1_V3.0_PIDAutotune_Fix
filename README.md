# BTT_B1_V3.0_PIDAutotune_Fix
Fix for PIDAUTOTUNE Function on BTT B1 V3.0 HW and Compatible's

GUIA DE SOLUCION PARA PID AUTOTUNE – BTT B1 v3.0 TFT - SPANISH

Problema: la función PID AUTOTUNE incorporada en la versión del firmware para pantallas BTT TFT B1 no funciona. Al comenzar el proceso y luego de un tiempo tira error de timeout pero nunca comienza a calentar ni el bloque calefactor ni la cama caliente. 
Solución: luego de investigar el código fuente del fichero  “Pid.c” perteneciente al firmware TFT localice que el código GCODE encargado de disparar el proceso del PID AUTOTUNE se encontraba mal formado .


SOLUTION GUIDE FOR PID AUTOTUNE - BTT B1  v3.0 TFT - ENGLISH

Problem: The PID AUTOTUNE function incorporated in the firmware version for BTT TFT B1 displays does not work. When starting the process and after a while it throws timeout error but it never starts heating neither the heating block nor the hot bed. 

Solution: after investigating the source code of the "Pid.c" file belonging to the TFT firmware, I found that the GCODE code in charge of triggering the AUTOTUNE PID process was incorrectly formed.

If you fix TFT codesource is neccesary replace two files:

* First change:  file TFT\src\User\Configuration.h
* Second change: TFT\src\User\Menu\Pid.c 

