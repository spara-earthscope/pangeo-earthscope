FROM public.ecr.aws/earthscope-dev/geolab/virtual_desktop:virtual_desktop-c6b4a6a3


RUN pip install -U scikit-learn

RUN mkdir -p /home/notebooks
WORKDIR /home/notebooks
COPY .  /home/notebooks