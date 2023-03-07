Target: Predict global_power_in and global_power_out

Data Attribute:

1.date: Date in format dd/mm/yyyy

2.time: time in format hh:mm:ss

3.global_power_in: overall minute-averaged power (in kilowatt)

4.global_power_out: overall minute-averaged power (in kilowatt)

5.voltage: minute-averaged voltage (in volt)

6.global_intensity: overall minute-averaged current intensity (in ampere)

7.metering_1: energy sub-metering No. 1 (in watt-hour of energy). It corresponds to room1 power consumption.

8.metering_2: energy sub-metering No. 2 (in watt-hour of energy). It corresponds to room2 power consumption.

9.metering_3: energy sub-metering No. 3 (in watt-hour of energy). It corresponds to room3 power consumption.

Summary:

1) Global Power In(GPI) can be forecasted as a stand-alone time series since it does not depend on smart power system. It might depend on utility service (PG&E,..)
2) Global Power Out(GPO) is too bumpy to have a good forecast to track all the spikes, so forecast lines are very close to a smooth average.
3) Difference between GPI and GPO can have a good forecast. It also benefits from adding other variables e.g voltage, intensity, room metters.
4) There is potential to improve on forecast error with increase number of epochs and finetune model architecture. Most of loss curve are not flat yet.
