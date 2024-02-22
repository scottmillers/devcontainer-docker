
# Dev Container CLI 

A development container cli is a reference implement so that indidivual users and other tools can read in devcontainer.json metadata and create dev containers from it.

## Install

1.  Select **Dev Containers: Install devcontainer CLI** from the command palette. This does not work.  It installs the dev container on the host operating system. I want to install it in the container.
2. Add the following featurs to my devcontainer.json file.

    ```json
    "features": {
            "ghcr.io/devcontainers-contrib/features/npm-package:1": {},
            "ghcr.io/devcontainers/features/node:1": {}
        }
    ```

3. Run the following command in the terminal.

    ```bash
    $ npm install -g @devcontainers/cli
    added 1 package in 693ms
    ```

4. Verify you can run the CLI and see its help text:
    ```bash
    devcontainer --help
    ```
## Use it in a project

Use it on a Rust sample.  Clone the rust same to your machine and start a dev container with the CLI's up command.

1. Clone the sample project to your machine.
    ```bash
    $ git clone https://github.com/microsoft/vscode-remote-try-rust
    ```
2. Run the commands in the dev container
    ```bash
    $ devcontainer up --workspace-folder <path-to-vscode-remote-try-rust>
   [2 ms] @devcontainers/cli 0.56.2. Node.js v20.11.1. linux 5.15.133.1-microsoft-standard-WSL2 x64.
Error: spawn docker ENOENT
    at ChildProcess._handle.onexit (node:internal/child_process:286:19)
    at onErrorNT (node:internal/child_process:484:16)
    at process.processTicksAndRejections (node:internal/process/task_queues:82:21)
{"outcome":"error","message":"spawn docker ENOENT","description":"An error occurred setting up the container."}
    ```

The command fails in another Devcontainer.  Looks like docker can not start another docker.


This also does not work on my laptop.

Possible reasons. 

## References

DevContainer CLI install
https://code.visualstudio.com/docs/devcontainers/devcontainer-cli#_installation