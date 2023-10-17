# CosmWasm Auditors' Dev Container (In Progress)

This development container aims to provide a turn-key development environment for auditors working with CosmWasm smart contracts. This container comes pre-configured with all the tools, libraries, and configurations required to perform security audits effectively and efficiently.

## Prerequisites

- [VS Code](https://code.visualstudio.com/)
- [Remote - Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- [Docker](https://docs.docker.com/get-docker/) or [Podman](https://podman.io/getting-started/installation)

## Features

- **Rust Environment**: Pre-configured with Rust, Cargo, and other Rust auditing tools.
- **Security Tools**: Includes commonly-used security tools for smart contract auditing.
- **Scripting Support**: Ready-to-use scripts for common auditing tasks. (In progress)

## Getting Started

### Using as a Dev Container

1. **Clone the Repository**

    ```bash
    git clone https://github.com/your-username/CosmWasm-auditors-devcontainer.git
    ```

2. **Navigate to the Project Folder**

    ```bash
    cd CosmWasm-auditors-devcontainer
    ```

3. **Copy devcontainer.json into audit repo**

    ```bash
     cp -r path/to/CosmWasm-auditors-devcontainer/.devcontainer /path/to/auditing-repo/
    ```
    

4. **Open in Dev Container**

    Open code and a popup will appear asking if you want to reopen the project in a Dev Container. Click "Reopen in Container".

    Alternatively, use `F1` to open the Command Palette and run "Remote-Containers: Reopen in Container".


### Using the base docker image

1. **Navigate to the folder containing the `Dockerfile` for the base image**

    ```bash
    cd /path/to/.devcontainer/
    ```

2. **Build the Base Image**

    ```bash
    docker build -t your-base-image-name .
    ```
    or if using Podman,

    ```bash
    podman build -t your-base-image-name .
    ```
3. **Manually Attach to the Container in VS Code**
4. **CTRL+SHIFT+P - Remote-Containers: Attach to Running Container**
5. **You have now manually attached to the container, keep in mind this ignores the devcontainer config**

## Recommendations
- I recommend configuring a rootless podman configuration.
## Troubleshooting

- For issues, refer to [VS Code Remote - Containers troubleshooting guide](https://code.visualstudio.com/docs/remote/troubleshooting) or [create an issue](https://github.com/your-username/CosmWasm-auditors-devcontainer/issues).
