FROM public.ecr.aws/earthscope-dev/geolab/virtual_desktop:virtual_desktop-c6b4a6a3

RUN mkdir ~/notebooks
RUN pip install -U scikit-learn

COPY /binder/hello_world.ipynb /notebooks/hello_world.ipynb