# Control a Water Tank Level

Consider a cylindrical tank with no outlet flow and an adjustable inlet flow that is controlled by a valve. The inlet flow rate is not measured but there is a level measurement that shows how much fluid has been added to the tank. The objective of this exercise is to develop a controller that can maintain a certain water level by automatically adjusting the inlet flow rate.

<img src="https://apmonitor.com/pdc/uploads/Main/tank_no_outlet.png" alt=""/>

Note: The symbol LT is an abbreviation for Level Transmitter. A concentration sensor is typically shown as CT for Concentration Transmitter or AT for Analyzer Transmitter. A temperature sensor such as a thermocouple is shown as TT which stands for Temperature Transmitter. If the second letter is C then it is a controller such as LC for Level Controller.

This example continues from the introduction to modeling where the process equation is derived and sample Python code is available.
<img src="Control a Water Tank Level/Single_equation.PNG" alt=""/>

where c is a constant that relates valve opening to inlet flow.

Design a P-only controller for the tank to maintain a level set point of 10.0 m. Test the P-only controller with different values of Kc by integrating the mass balance equation for a period of 10 seconds. Use a value of 1000 kg/m3 for density and 1.0 m2 for the cross-sectional area of the tank. For the valve, assume a valve coefficient of c=50.0 (kg/s / percent open). Make sure that the valve does not exceed the limits of 0-100 percent by clipping the requested valve opening to an acceptable range. For example, if the P-only controller calculates a valve opening of 150 percent, use 100 percent instead.

Use the following Python script as a starting point for the simulation and add the Proportional-only controller. Select "Get Code" from the link at the bottom corner to get unformatted text. Fill in the areas labeled "TO DO" to implement the P-only controller.
