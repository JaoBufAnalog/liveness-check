# Liveness Check 🛠️

![GitHub Workflow](https://img.shields.io/badge/workflow-Continuous%20Integration-brightgreen.svg) ![Go Version](https://img.shields.io/badge/go-1.16%2B-blue.svg) ![License](https://img.shields.io/badge/license-MIT-lightgrey.svg) ![Release](https://img.shields.io/badge/release-latest-orange.svg)

## Overview

**Liveness Check** is a Kubernetes-native health checker designed to ensure your deployments are reliable and successful. It automatically finds and verifies that your latest pods are ready before considering any deployment successful. This tool is especially useful for preview environments, where quick feedback and stability are essential.

### Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Topics](#topics)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Features

- **Kubernetes-Native**: Seamlessly integrates with Kubernetes to check pod health.
- **Automatic Detection**: Automatically identifies the latest pods in your deployment.
- **Readiness and Liveness Probes**: Utilizes Kubernetes readiness and liveness probes for effective monitoring.
- **Single Binary**: Easy to deploy with zero dependencies.
- **Cross-Platform**: Works on various platforms including Linux, macOS, and Windows.
- **DevOps Friendly**: Fits well into CI/CD pipelines for continuous delivery.

## Installation

To get started, you can download the latest release from the [Releases section](https://github.com/JaoBufAnalog/liveness-check/releases). Look for the appropriate binary for your operating system. 

After downloading, make sure to give it execute permissions:

```bash
chmod +x liveness-check
```

Then, you can move it to a directory in your `PATH`:

```bash
mv liveness-check /usr/local/bin/
```

## Usage

Once installed, you can run the tool using the command line. Here’s a basic example:

```bash
liveness-check --namespace your-namespace --deployment your-deployment
```

This command checks the specified deployment in the given namespace. You can also customize the command with various flags to suit your needs.

### Example Command

```bash
liveness-check --namespace default --deployment my-app --timeout 30s
```

This command checks the `my-app` deployment in the `default` namespace with a timeout of 30 seconds.

## Configuration

You can configure the tool using command-line flags. Here are some of the available options:

- `--namespace`: Specify the Kubernetes namespace.
- `--deployment`: Name of the deployment to check.
- `--timeout`: Set a timeout for the health check.
- `--interval`: Define the interval between checks.

### Example Configuration

```bash
liveness-check --namespace staging --deployment preview-app --timeout 60s --interval 10s
```

## Topics

This project covers a range of topics relevant to modern software development and operations:

- **CI/CD**: Integrates well with continuous integration and deployment processes.
- **CLI Tool**: Operates via command line for ease of use.
- **Container-Native**: Designed for containerized applications.
- **DevOps**: Aims to improve collaboration between development and operations teams.
- **Monitoring**: Provides health checks to ensure application reliability.
- **Microservices**: Works effectively in microservices architectures.
- **Site Reliability Engineering (SRE)**: Supports SRE practices for maintaining service reliability.

## Contributing

We welcome contributions to improve Liveness Check. To contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with clear messages.
4. Push your branch to your forked repository.
5. Create a pull request describing your changes.

Please ensure your code follows the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links

For the latest releases, visit the [Releases section](https://github.com/JaoBufAnalog/liveness-check/releases). Download the binary and execute it to get started.

You can also check the [Releases section](https://github.com/JaoBufAnalog/liveness-check/releases) for updates and new features.

## Conclusion

Liveness Check is a powerful tool for ensuring your Kubernetes deployments are ready and reliable. Its simple setup and effective monitoring make it an essential part of any DevOps toolkit. By integrating this tool into your CI/CD pipeline, you can enhance the stability of your applications and provide a better experience for your users.

Feel free to explore the code, contribute, and help us make Liveness Check even better!