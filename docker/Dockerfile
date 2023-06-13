# Use PyTorch as the base image
FROM pytorch/pytorch:latest

# Install unzip and cmake
RUN apt-get update && apt-get install -y \
    g++\
    unzip \
    cmake \
    wget  \
    curl

# Download your zip file

WORKDIR /root
RUN wget https://github.com/cbigger/text-generation-webui/releases/download/installers/oobabooga_linux.zip

# Unzip the file
RUN unzip oobabooga_linux.zip && rm oobabooga_linux.zip

# Change directory to the unzipped folder (assuming the unzipped folder name is oobabooga_linux, change accordingly if not)
WORKDIR /root/oobabooga_linux

# Expose port 7860
EXPOSE 7860

# Add the start command as the default command for the container
CMD ["bash", "start_linux.sh"]

# CMD ["/bin/bash"]


