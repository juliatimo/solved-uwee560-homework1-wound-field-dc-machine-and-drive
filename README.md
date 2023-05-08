Download Link: https://assignmentchef.com/product/solved-uwee560-homework1-wound-field-dc-machine-and-drive
<br>
Fig. 1. Block diagram of a DC Machine

Speed curves are linearly proportional to electromagnetic torque with slope equal to . The curves are plotted according to the parameters given for MGFQK 063-32 and MGFQK 160-22.

Fig. 2. Speed torque response for MGFQK 063-32 (1W) and MGFQK 160-22 (90.8W)

As expected, the larger machine has a much greater stall torque. The slopes for the small and large motor are -34.23 rpm/(Nm) and -0.40 rpm/(Nm). Corresponding slopes in SI units are-3.58 rad/(Nms) and -0.042 rad/(Nms).

Eigenvalues are found analyzing the speed voltage dynamics and applying the Python Scypi Signals library.

The characteristic equation is solved such that the small motor has values -213.13, -147.52 and larger motor has values (-45 + j81.97),  (-45 – j81.97). A step voltage of 170V and 460V are applied to the small and large motor respectively.

Fig. 3. Eigenvalues and step response behavior for ideal voltage source

The small motor has real, negative distinct roots that result in an overdamped response as seen in the step plot. The large motor has complex, negative roots that result in an underdamped response. In addition, electrical time constant () is 2.77e-3. Electromechanical time constant () is 1.15e-2. Since both of these motors are relatively small, the transfer function can be simplified to

All simulations results from MGFQK 063-32 and MGFQK 160-22 are shown in the figure. Sensor measurements are compared on the y-axis and DC motors on the x-axis. The H-bridge response aligns with the ideal voltage source at sufficient switching frequency, 20kHz, in this example. H-bridge plots are shown with a thicker line so all results can be visualized. In each machine, the duty cycle was adjusted such that  outputs the correct armature voltage of 170V and 460V.  The calculated duty cycles are 0.625 and 0.838. Note, larger loads decrease the machine speed as expected. All simulations agree with the analytical response calculated earlier.

Fig. 4. Current, speed, and torque simulation results

Lastly, the effects of different switching frequencies are analyzed in the PWM controlled H-bridge simulations. I compared 1kHz and 20kHz switching frequencies.

Fig. 5. Switching frequency effects

Changing the switching frequency has little effect on the steady state motor speed, however it is evident in current and torque responses. At lower switching frequencies, large oscillations occur. To limit oscillations, greater switching frequencies are necessary.