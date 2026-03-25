# Use an official lightweight Debian image
FROM ://mcr.microsoft.com

# Install necessary build tools and ARM toolchain
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    build-essential \
    cmake \
    git \
    unzip \
    wget \
    # Install ARM GNU Toolchain
    gcc-arm-none-eabi \
    libnewlib-arm-none-eabi \
    # Install OpenOCD for flashing/debugging
    openocd \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Set the default user
USER vscode
