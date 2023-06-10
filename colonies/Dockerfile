FROM ubuntu:22.04

RUN apt-get update && DEBIAN_FRONTEND="noninteractive" TZ="Europe/Stockholm" apt-get install -y python3 python3-pip postgresql libpq-dev npm git  
RUN pip3 install datacube geojson geopandas folium ipyleaflet descartes gpytorch fiona rioxarray pycrs gpytorch torch torchvision jupyterlab ipympl ipyleaflet jupyter_bokeh jupyterlab-geojson dask jupyterlab_theme_solarized_dark jupyterthemes pandas shapely pyproj rtree tslearn fastdtw statsmodels h5py
RUN npm install --global yarn
RUN jupyter notebook --generate-config
ENV JUPYTER_TOKEN hej
#ENTRYPOINT ["jupyter", "lab", "--allow-root", "--ip", "0.0.0.0", "--notebook-dir", "/root", "--NotebookApp.token=''", "--NotebookApp.password=''"]
ENTRYPOINT ["jupyter", "lab", "--allow-root", "--ip", "0.0.0.0", "--notebook-dir", "/root"]
