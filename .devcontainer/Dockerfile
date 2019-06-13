#-------------------------------------------------------------------------------------------------------------
# Copyright (c) Microsoft Corporation. All rights reserved.
# Licensed under the MIT License. See https://go.microsoft.com/fwlink/?linkid=2090316 for license information.
#-------------------------------------------------------------------------------------------------------------

FROM mcr.microsoft.com/dotnet/core/sdk:3.0

# Install git, process tools
RUN apt-get update && apt-get -y install git procps libc6-dev

# Clean up
RUN apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

# Install .NET Core Diagnostics Tools
RUN dotnet tool install --global dotnet-counters --version 1.0.4-preview6.19311.1 --add-source https://dotnetfeed.blob.core.windows.net/dotnet-core/index.json \
    && dotnet tool install --global dotnet-trace --version 1.0.4-preview6.19311.1 --add-source https://dotnetfeed.blob.core.windows.net/dotnet-core/index.json \
    && dotnet tool install --global dotnet-dump --version 1.0.4-preview6.19311.1 --add-source https://dotnetfeed.blob.core.windows.net/dotnet-core/index.json \
    && dotnet tool install -g dotnet-symbol

# Set path and shell
ENV PATH="$PATH:~/.dotnet/tools"