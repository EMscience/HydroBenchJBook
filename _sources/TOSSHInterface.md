# Linking HydroBench and TOSSH

HydroBench allows using the Toolbox for Streamflow Signatures ([TOSSH](https://tosshtoolbox.github.io/TOSSH/)) toolbox through the matlab - python API. 
To get started, the following are required:

1. a licence to Matlab. 
2. cloning/downloading the TOSSH Toolbox to your working directory. 
3. enabling the Matlab and Python API through the following steps.

	a) Refer to the following [link](https://www.mathworks.com/help/matlab/matlab_external/install-the-matlab-engine-for-python.html) for details.

	b) To setup Matlab in Python:

		python setup.py install # inside the matlab rootfolder: i.e., cd "matlabroot\extern\engines\python"
		
	c) To start the Matlab engine within a notebook:
		
		import matlab.engine
		eng = matlab.engine.start_matlab() # start matlab engine
		eng.quit() # end matlab engine

	d) This [link](https://www.mathworks.com/help/matlab/matlab_external/call-user-script-and-function-from-python.html) provides
	a guide on how to use a local matlab function within matlab. Its implementation to acess the TOSSH functions and methods within HydroBench is as follows.
			
			eng.addpath('./TOSSH-master/TOSSH_code/calculation_functions/');
			eng.addpath('./TOSSH-master/TOSSH_code/signature_functions/');
			eng.addpath('./TOSSH-master/TOSSH_code/utility_functions/');
			
After following the above steps, any function from TOSSH can be called within HydroBench. The HydroBench demonstration notebook provides a detailed example of implenting the above steps. 