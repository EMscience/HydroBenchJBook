# Linking HydroBench and TOSSH

HydroBench allows using the Toolbox for Streamflow Signatures ([TOSSH](https://tosshtoolbox.github.io/TOSSH/)) functions through the matlab - python API. To get started, the following are required:

1.  a license to MatLab.
2.  cloning/downloading the TOSSH Toolbox to your working directory.
3.  enabling the MatLab and Python API through the following steps.

    a) Refer to the following [link](https://www.mathworks.com/help/matlab/matlab_external/install-the-matlab-engine-for-python.html) for details.

    b) To setup MatLab in Python:

```
 python setup.py install # inside the MatLab rootfolder: i.e., cd "matlabroot\extern\engines\python"
```

c) To start the MatLab engine within a notebook:

```
 import matlab.engine
 eng = matlab.engine.start_matlab() # start MatLab engine
 eng.quit() # end matlab engine
```

d) This [link](https://www.mathworks.com/help/matlab/matlab_external/call-user-script-and-function-from-python.html) provides a guide on how to use a local Matlab function within Matlab. Its implementation to access the TOSSH functions and methods within HydroBench is as follows.

```
 	eng.addpath('./TOSSH-master/TOSSH_code/calculation_functions/');
 	eng.addpath('./TOSSH-master/TOSSH_code/signature_functions/');
 	eng.addpath('./TOSSH-master/TOSSH_code/utility_functions/'); 
```

After following the above steps, any function from TOSSH can be called within HydroBench. The HydroBench demonstration notebook provides a detailed example of implementing the above steps.
