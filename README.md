# Demo for .NET Core Diagnostics Tooling
This is a demo repo for playing around with the .NET Core 3.0 diagnostics tools. I've used this in a couple of talks.

## Getting Started
This repo comes complete with a DevContainer that you can use with [VS Code](https://code.visualstudio.com) and its [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) extensions. If you have those extensions installed you should get a notification asking you to open the workspace inside of the container. When you do this a container will be build which will include all the tools you need. See the Dockerfile in the .devcontainer folder for more details on what is included in the container.

## Scenario's
These scenario's are based on the existing [documentation](https://github.com/dotnet/diagnostics/tree/master/documentation/tutorial) that's available for the Diagnostics Tools. I've simply combined a couple of useful tools to easily demo this, at least for the following scenario's from that tutorial:

- App is leaking memory
- App is running slow