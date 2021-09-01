# Energy Variability and Cellular Decision-Making

Python scripts computing steady states, and their stability, for different parameter sets. Matlab files plot figures using data from python files and two files are also included for additional steady state stability checks.

## File contents and description of analyses

--- Calculating stable and unstable steady states ---<br/>
data-basin-transitions.py
	Python code calculating the minimum work needed to transition between the two extreme attractor basins; in monostable landscapes no metric is calculated. Script uses data from data-hms-sigmoid.py (with n=4) to input the stable steady states.

data-bifurcation-diagrams.py
	Python code calculating the steady states and their stability for non-linear ODEs with different parameter sets. Multiple parameter sets are simulated, then results are exported to csv files in a directory (named 'data-files') created by the script.

data-bif-zoom.py
	Similar to 'data-bifurcation-diagrams.py'. Smaller regions of A* within select bifurcation diagrams are now analysed. Results are exported to csv files.

data-hms-sigmoid.py
	Python code calculating the steady states and number of stable steady states for different parameter sets (varying n, a, b, A*). Results are exported to separate csv files.

data-hms-sigmoid-modified.py
	Similar to data-hms-sigmoid.py, except lambda is vertically displaced (it is still sigmoidal). Also, only the number of stable steady states are calculated and the Hill coefficient, n, is no longer varied. Results are exported to a csv file.

data-hms-theta.py
	Python code calculating the number of stable steady states for different parameter sets (varying thetaA, thetaB and A*). Results are exported to a csv file.

data-hms-linear.py
	Similar to data-hms-sigmoid.py, except only lambda is now modelled as a linear function and n is no longer varied. Results are exported to a csv file.


--- Plotting figures ---<br/>
plot_hm_basin_transitions.m
	Matlab script plots the output of 'data-basin-transitions.py'. All figures are saved in Scalable Vector Graphics format.

plot_bif_diagrams.m
	Matlab script plots the output of 'data-bifurcation-diagrams.py'. All figures are saved in Scalable Vector Graphics format.

plot_zoomed_bif.m
	Matlab script plots the output of 'data-bif-zoom.py'. All figures are saved in Scalable Vector Graphics format.

plot_hm_sigmoid.m
	Matlab script plots the output of 'data-hms-sigmoid.py'. All figures are saved in Scalable Vector Graphics format.

plot_hm_modified_sigmoid.m
	Matlab script plots the output of 'data-hms-sigmoid-modified.py'. All figures are saved in Scalable Vector Graphics format.

plot_hms_theta.m
	Matlab script plots the output of 'data-hms-theta.py'. All figures are saved in Scalable Vector Graphics format.

plot_hm_linear.m
	Matlab script plots the output of 'data-hms-linear.py'. All figures are saved in Scalable Vector Graphics format.

plot_arrays.m
	Matlab script plots arrays displaying re-entrant behaviour using the output of 'data-hms-sigmoid.py'. All figures are saved in Scalable Vector Graphics format.

plot-example-phase-portraits.py
	Python script plots example phase portraits used to show the behaviour contained within each heatmap.

plot-example-timedependent-simulations.py
	Python script plots time-dependent simulations to show the behaviour presented in each bifurcation diagram.

plot_lambda_functions.m
	Matlab script plots sigmoidal, linear and a modified sigmoid form of lambda used in the above python scripts.

All figures were completed to their final form in LaTex (using TikZ) and Inkscape.


--- Stability Checks ---<br/>
steady_states_calculator.mw
	Maple script calculates the roots of the system of non-linear ODEs for a fixed parameter set for A* between 0-1 in 0.1 steps.

steady_state_stability_check.m
	Matlab script checks a steady state (entered manually) from 'steady_states_calculator.mw' or calculated in the above python files using the Jacobian.


--- Contact ---<br/>
Email ryankerr8@gmail.com with any questions.
