FROM public.ecr.aws/earthscope-dev/geolab/geolab-default:default_pytorch_split-f59cda68

# Adding packages in the Dockerfile example
# RUN pip install -U scikit-learn python-package

# Adding packages from an environment.yml file
COPY /binder/environment.yml /tmp

RUN mamba env update --name ${CONDA_ENV} -f /tmp/environment.yml \
    && pip cache purge \
    && mamba clean -afy
    
# Adding files to the image:
# The /home/joyvan directory is created and mounted when the container is created.
# Writing a file to that directory will be overwritten.
# Write files to other directories such as /tmp and copy it to home directory.
RUN mkdir -p /tmp/notebooks
WORKDIR /tmp/notebooks
COPY /binder/hello_world.ipynb  /tmp/notebooks