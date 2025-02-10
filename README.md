# hra-amap

Overview : 
The HRA-AMAP project aims to enable projection of tissue blocks registrered to a source organ to a new reference organ (usually the Human Reference Atlas, part of HuBMAP).
For more details : https://github.com/cns-iu/hra-amap

Setup and Installation : 
Follow the steps from the original git repo project for setting up your repository - https://github.com/cns-iu/hra-amap

Issues faced : 
1. GitHub’s Jupyter Notebook preview does not support .glb file visualizations. However, when you open the .ipynb file locally in Jupyter Notebook, the visualizations appear correctly if the necessary rendering libraries are available in your local environment.
2. The relative path mentioned in the py config files caused few directory locating issues, but resolved once it was all assigned properly.
3. Clang error during installation for MacOS occured like expected and it was sorted out once the correct path for libomp was given.

Suggested optimisations: 
1. Using dynamic paths both in the config py files as well as in the jupyters notebooks. We can use environmental variables for repo paths. This can help make the project more adaptable to different local setups without hardcoding paths in the configuration files.
2. Parallel execution of the notebooks, utilising threadpool for example will reduce the overall computation time.
3. In the instantiation of the Pipeline object in the notebooks - if some parameters are only needed at certain stages of the pipeline, you can load them on-demand rather than loading everything upfront.
4. More robust error handling for common issues, such as missing files or invalid inputs could be done by setting up logging. It would cause errors to be recorded in both the console and a log file.
