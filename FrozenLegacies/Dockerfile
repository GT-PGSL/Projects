# Use the official JupyterLab image as base
FROM jupyter/scipy-notebook:latest

# Install additional system tools if needed 
USER root
RUN apt-get update && apt-get install -y wget
USER jovyan

# Install required Python packages
RUN pip install numpy matplotlib scikit-image opencv-python

# Copy code into the container
COPY Z_Scope_Processing /home/jovyan/work/Z_Scope_Processing

# Download demo.tiff from Dropbox (replace YOUR_DROPBOX_ID with your actual ID)
RUN wget "https://drive.google.com/file/d/1ZEkRrKTXIPz3WpLIEZDwAohS9X41uX4W/view?usp=share_link" -O /home/jovyan/work/demo.tiff


# Set the working directory
WORKDIR /home/jovyan/work
