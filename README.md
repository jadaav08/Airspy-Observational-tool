# Airspy-Observational-tool
Uses a fortran 2008 code based on the airspy_rx command.

Please read the airspy_rx tool manual before using this code. Type 'man airspy_rx' in terminal. 

The code has been tested on Ubuntu 16.04 and works well. Ensure that you have the proper gfortran library installed.

Compile the fortran code using the command below :

gfortran -o AIRSPY_OBSERVTIONAL_TOOL AIRSPY_TOOL.F08

Run using the command below :

./AIRSPY_OBSERVATIONAL_TOOL

It also works with the Spyverter but since the airspy_rx command controls the airspy only, the user has to know the frequency conversions occuring in the Spyverter and the Airspy. Bias Tee must be enabled so as to power the spyverter.

Functions :

1. The airspy can be set to start sampling at a particular time in terms of delay in seconds.

2. The time at which observation stops can also be set.

3. The code allows sampling of a specific number of samples and storing them in different files for ease of processing later on.

4. A specific delay can be set in seconds between samples if you don't want continuous data.

Note :

1. For the file extension no dot should be used; e.g : txt, wav or any other...

2. The delay till the time of observation has to be calculated manually in seconds.

3. The end time has to be input like this : 234523 which means observation stops at 23h 45min 23s.

4. If time interval between samples is set to 0, it becomes difficult to quit the program manually by the Ctrl-C command. 

5. The sensitivity gain has been removed. I preferred using the linearity gain. Both cannot be used at the same time. The code has to be modified if you want to use the sensitivity gain according to the airspy_rx tool.

