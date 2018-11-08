# CloneFit
Application to compare experimental clone size data withtumor growth model from Lenos et al, Nature Cell Biology 2018. Requires Matlab 2016a or later.


# Install
A computer with internet connection, a web browser and MATLAB 2016a or a later version installed is required. The software is not computationally intensive and has no special requirements on the hardware.

Install comliled CloneFit App: Download the "CloneFit.mlappinstall" from this repository. Open Matlab (version 2016a or later) and select the “Apps” tab in the left top of the screen. Click on the “Install App” button in the left top of the screen. Navigate to the download folder and select the CloneFit App for installation.  After successful installation the App can be opened from the Apps dropdown menu and is ready for usage. 

Instal source file: The source file of the CloneFit app ("CloneFit.mlapp") is also available in thie repository and can be used to customize the CloneFit App. The source file can be executed from the Matlab command line. When using the source file, also download the "app_num_data_cgs181026.mat" file which contains the numerical data, or generate your own numerical data using the "CGS.m" tumor growth file, available in the "Tumor-Growth-Model" repository on my GitHub profile.


# Operate
Load experimental data
Timing: 1 minute
Load the experimental data by pressing the “Load experimental” button in the “Experimental data” panel. From the raw clone size data, distributions at each time point are generated and visualized in the CloneFit App. The red lines in the generated plots correspond to the model predictions using the parameter values that correspond to the slide bar values. Note that by changing the slide bar values the numerical distributions are immediately updated to the corresponding current slide bar values of the parameters.

Optional 
Explore numerical data
Timing: 5 minutes
The numerical clone size data generated from simulations with the stochastic model is automatically appended to and opened in the App. The distribution of clone sizes changes over time and with parameter settings. The features of the model can be explored by changing the parameter values using the slide bars in the “Numerical data” panel of the App.

Parameter inference 
Timing: seconds to minutes (depending on the speed of the processor and size of the data).
The method of Least-squares can be applied to find the parameter values, and thus the tumor growth mode, that best describes the experimental data. In the “Inference” panel, press the “Parameter inference” button to compare the experimental data with the numerical data for all combinations of parameter values. The parameter values corresponding to the best fit according to the method of Least-squares are printed as output in a textbox. A heat map of the inverse least-square values versus lambda and h is also generated.

Optional 
Inference of a selected set of parameters
Timing: seconds to minutes (depending on the speed of the processor and size of the data).
The parameter inference can also be performed with one or two parameter values fixed. A parameter can be fixed by selecting the “Fix h/a/lambda” check boxes right to the “Parameter inference” button. The numerical values of fixed parameters can be manually selected using the slide bars in the “Numerical data” panel. Parameter inference of the non-fixed parameter(s) is performed as described above.

Export data 
Timing: 5 seconds
The experimental and numerical clone size distributions can be exported into tab separated text files by clicking the “Export experimental” and “Export numerical” buttons, respectively, in the “Export distributions” panel. The output files are saved in the current working directory. For the numerical data, the clone size distributions for the current parameter values at the days for which experimental data is available are exported. 
