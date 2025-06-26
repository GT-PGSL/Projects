FROM jupyter/scipy-notebook:latest

# Install required Python packages
RUN pip install numpy matplotlib scikit-image opencv-python

# Copy code into the container
COPY Z_Scope_Processing /home/jovyan/work/Z_Scope_Processing

# Download the demo.tiff file from Dropbox
RUN wget "https://www.dropbox.com/home/Winnie%20Chu/FrozenLegacies/Demo_Data/demo.tiff" -O /home/jovyan/work/demo.tiff

# Set the working directory
WORKDIR /home/jovyan/work

