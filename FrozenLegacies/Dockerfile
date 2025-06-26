
FROM jupyter/scipy-notebook:latest

# Install required Python packages 
RUN pip install numpy matplotlib scikit-image opencv-python

# Or use requirements.txt to install packages:
# COPY requirements.txt .
# RUN pip install -r requirements.txt

# Copy code and demo data into the container
COPY Z_Scope_Processing /home/jovyan/work/Z_Scope_Processing
RUN apt-get update && apt-get install -y wget
RUN wget https://www.dropbox.com/scl/fi/1vdb4tl0xhiwk6ms66xkf/demo.tiff?rlkey=qxyyfr0qrv92f5wv44pmzvctk&st=49gq8zj6&dl=0 -O /home/jovyan/work/demo.tiff

# Set the working directory
WORKDIR /home/jovyan/work
