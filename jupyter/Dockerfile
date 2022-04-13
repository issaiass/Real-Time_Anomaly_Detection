# install python 3.7 minimal
FROM python:3.7-slim

# make a source directory
RUN mkdir src

# set the working directory
WORKDIR src

# copy the requirements
COPY requirements.txt .

# install basic requirements
RUN pip install -r requirements.txt

# install jupyter
RUN pip install jupyter notebook

# expose the notebook
CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root"]