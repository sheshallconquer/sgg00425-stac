# Windows and Mac require some slight variation in installing the environment

# For Mac and probably Linux:
conda env update -f _pystac_install-env-MAC.yml

# For Windows:
conda env update -f _pystac_install-env-WIN.yml

# If you still run into problems (message says "Solving environment" for more than a minute):
# Manual installation of the environment as follows:
conda create -n pystac_example
conda activate conda pystac_example
conda install jupyterlab dask matplotlib rioxarray ipywidgets folium seaborn geopandas ipympl gdal
conda install pystac-client odc-stac odc-algo datacube -c conda-forge


# Activating the environment
conda activate pystac_example

# Start the environment:
jupyter lab

# If browser shows "Access denied" message
jupyter server --generate-config
jupyter lab --ServerApp.root_dir="%USERPROFILE%"

