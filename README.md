# pygmt-install-instructions
PyGMT and GMT6.0 install instructions through miniconda

## Install GMT6
Create a new conda environment dedicated to GMT6
```
conda create --name gmt6
conda activate gmt6
conda install gmt=6
```
Deactivate the environment to return to your default environment
```
conda deactivate
```
## Install PyGMT in an environment of interest
```
git clone https://github.com/GenericMappingTools/pygmt.git
cd pygmt
pip install .
```

## Link the GMT6 libraries
PyGMT will automatically scan for the GMT6 libraries in the known locations (`\usr\lib`,`\usr\local\lib`, etc), however, now you need to specify the path explicitely
```
export GMT_LIBRARY_PATH="~/miniconda3/envs/gmt6/lib"
```
