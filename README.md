# Robotic Sgraffito

## Requirements 
* [Rhinoceros 3D 7.0](https://www.rhino3d.com/): Update Rhino to the newest version

**Quick links:** [compas docs](https://compas-dev.github.io/main/) | [compas_fab docs](https://gramaziokohler.github.io/compas_fab/latest/)

* [Rhinoceros 3D 7.0](https://www.rhino3d.com/)
* [Anaconda Python Distribution](https://www.anaconda.com/download/): 3.x
* Git: [official command-line client](https://git-scm.com/) or visual GUI (e.g. [Github Desktop](https://desktop.github.com/) or [SourceTree](https://www.sourcetreeapp.com/))
* [VS Code](https://code.visualstudio.com/) with the following `Extensions`:
  * `Python` (official extension)
  * `EditorConfig for VS Code` (optional)
  * `Docker` (official extension, optional)

## Set-up and Installation

### 1. Setting up the Anaconda environment with COMPAS

#### Execute the commands below in Anaconda Prompt as Administator:
	
    (base) conda config --add channels conda-forge
    (base) conda create -n env_name compas_fab --yes
    (base) conda activate env_name
    
#### Verify Installation
    (env_name) pip show compas_fab

####
    Name: compas-fab
    Version: 0.xx
    Summary: Robotic fabrication package for the COMPAS Framework
    ...

#### Install COMPAS RRC

    (env_name) conda install compas_rrc

#### Install on Rhino

    (env_name) python -m compas_rhino.install -v 7.0


### 2. Installation of Dependencies

    (env_name) conda install git

#### UR Fabrication Control
    
    (env_name) python -m pip install git+https://github.com/augmentedfabricationlab/abb_fabrication_control@master#egg=abb_fabrication_control
    (env_name) python -m compas_rhino.install -p abb_fabrication_control -v 7.0

### 3. Cloning and installing the Course Repository

* Create a workspace directory: C:\Users\YOUR_USERNAME\workspace
* Open Github Desktop, clone the [robosgraffito](https://github.com/augmentedfabricationlab/robosgraffito) repository into you workspace folder 
* Install within your env (in editable mode):

```
(env_name) cd C:\Users\YOUR_USERNAME\workspace
(env_name) python -m pip install -e robosgraffito
(env_name) python -m compas_rhino.install -p robosgraffito -v 7.0
```

