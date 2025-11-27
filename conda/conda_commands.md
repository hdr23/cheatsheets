# Conda Command Reference

## Environment Creation

### Create Local Environment
Create an environment in a specific local directory (`./env`) with specific packages and Python version.
`conda create --prefix ./env python=3.12 pandas numpy matplotlib scikit-learn jupyter`

### Create from YAML
Create an environment using a configuration file.
`conda env create -f environment.yml`

## Activation & Usage

### Activate Environment
Activate using the full path to the environment folder.
`conda activate <path_to_env>`
*Example:* `conda activate C:\Users\rojas\Documents\Projects\aies-group\env`

### Deactivate Environment
Exit the current environment.
`conda deactivate`

## Management & Maintenance

### List Environments
View all available environments and their paths.
`conda env list`

### List Installed Packages
See all packages installed in the active environment.
`conda list`

### Install Package
`conda install <package_name>`

### Update All Packages
Update all packages in the active environment to the latest compatible versions.
`conda update --all`

### Export Environment
Save the current environment configuration to a file.
`conda env export > environment.yml`

## Cleanup & Deletion

### Remove Environment (Prefix)
Delete an environment located at a specific path.
`conda env remove -p ./env`

### Remove Environment (Named)
Delete a named environment.
`conda env remove -n <env_name>`

### Clean Disk Space
Remove unused packages and caches (essential for freeing up disk space).
`conda clean --all`