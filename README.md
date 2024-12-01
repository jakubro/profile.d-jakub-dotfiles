# profile.d-jakub-dotfiles

A plugin for [profile.d](https://github.com/jakubro/profile.d) that provides a comprehensive set of shell
customizations, environment configurations, and utility functions for enhanced development workflow.

## Features

### System Configuration

- Sets up essential environment variables and PATH configurations
- Configures default editors (nano and sublime text)
- Sets up GPG TTY for Git signing
- Provides color definitions for shell scripts
- Configures systemd behavior

### Development Tools Integration

- NVIDIA CUDA and GPU support
- Ruby environment (rbenv) configuration
- Rust cargo integration
- AWS CLI configuration
- Temporal.io CLI integration
- JetBrains Toolbox integration

### Docker Integration

- Provides extensive Docker aliases for throwaway containers
- Supports various Linux distributions (Ubuntu, Fedora, Amazon Linux)
- Includes development environments (Node.js, Python, Ruby)
- Configures database containers (PostgreSQL, MySQL, Redis)
- Mounts common directories and Docker socket

### Shell Enhancements

- Improved `rm` command with trash-put integration
- Enhanced `ls` command aliases
- Automatic terminal title updates
- Session persistence (remembers last working directory)

### Project Management

- Default direnv configuration with Node.js and Python support

## Installation

1. Add the following line to your `~/.profiledrc`:

```bash
PLUGINS=(
  # ... your other plugins ...
  https://github.com/jakubro/profile.d-jakub-dotfiles
)
```

2. Run the installation commands:

```bash
profile.d-install
. ~/.bashrc
```

## Usage

### Docker Containers

Launch throwaway containers for various purposes:

```bash
# Launch Ubuntu containers
throwaway-ubuntu
throwaway-ubuntu-22
throwaway-ubuntu-20
throwaway-ubuntu-18

# Launch Fedora containers
throwaway-fedora
throwaway-fedora-37
throwaway-fedora-36

# Launch development environments
throwaway-node-20
throwaway-python-3.11
throwaway-ruby-3.1

# Launch databases
throwaway-postgres-16
throwaway-mysql-8
throwaway-redis-7
```

### System Commands

```bash
# Reload shell configuration
reload

# Reload direnv configuration
d-reload

# Safe remove (moves to trash)
rm file.txt

# Force remove (bypasses trash)
rmf file.txt

# Enhanced ls commands
ll      # detailed listing
lz      # SELinux context listing
```

### Development Environment

The plugin automatically configures:

- NVIDIA CUDA environment when available
- Vulkan and VA-API for GPU support
- Python development tools
- Node.js development environment
- Ruby development with rbenv
- Rust cargo environment

## Configuration

### Environment Variables

The plugin sets up various environment variables for development tools:

- `EDITOR` and `VISUAL` for text editors
- `CUDA_DIR` for NVIDIA development
- `PATH` modifications for local binaries
- AWS configuration
- Various tool-specific configurations

## Requirements

- Base requirements from profile.d
- Optional tools based on usage:
    - NVIDIA drivers and CUDA for GPU features
    - Docker for container features
    - Development tools (Python, Node.js, Ruby, etc.)

## Contributing

If you would like to contribute to this project, please feel free to submit a pull request or open an issue for
discussion.

## License

MIT License - see the [LICENSE](LICENSE) file for details.
