# Scylla: Securing Blockchain Wallet Files using eBPF

<img src="misc/logo.png" width="128"/>


## Introduction

In this repository, we introduce **Scylla**, an  solution  designed to enhance the security of blockchain (BC) and Distributed Ledger Technology (DLT) wallet-related files by preventing unauthorized access through the utilization of extended Berkeley Packet Filter (eBPF). The proposed solution employs fine-grained access control mechanisms, providing robust protection for critical files, including account files. This is achieved by actively monitoring system calls of processes directed towards these sensitive files.

## Publication

Scylla was approved for publication as a full-paper in the [IEEE Global Communications Conference (GLOBECOM 2024)](https://globecom2024.ieee-globecom.org/). The full paper can be found here: [https://ieeexplore.ieee.org/document/10901795](https://ieeexplore.ieee.org/document/10901795)

If you wish to reference Scylla, you can use the following citation:
```
J. C. Caroly, E. J. Scheid, M. F. Franco and L. Z. Granville, "Securing Blockchain Wallet Files Using eBPF," GLOBECOM 2024 - 2024 IEEE Global Communications Conference, Cape Town, South Africa, 2024, pp. 553-558, doi: 10.1109/GLOBECOM52923.2024.10901795.
```

## Key Features

- **Fine-grained Access Control:** **Scylla** implements fine-grained access control measures to protect critical files, ensuring that only authorized processes can access them.

- **Automatic Execution:** The solution is designed to be executed automatically during system boot time.

- **Protection Based on Inodes:** **Scylla** can be ajusted to protects itself and user-defined files based on their *inodes*, providing an additional layer of security.

## How it Works

During execution, **Scylla** actively monitors the system calls of processes aiming to access sensitive files. This proactive approach allows it to intercept and prevent unauthorized attempts to read or modify the content of a file. Evaluations of **Scylla** demonstrate its capability to achieve these security objectives without introducing significant overhead to legitimate processes.

## Comparison to Other Tools

In comparative evaluations of functionality, **Scylla** has proven to outperform *inotify*, a Linux kernel subsystem designed for monitoring changes in the filesystem. Unlike *inotify*, **Scylla** goes beyond monitoring, actively preventing unauthorized file access and providing a more robust security solution for BC wallet-related files.

## Getting Started

To use **Scylla**, follow these steps:

1. Clone the repository: `git clone git@github.com:ComputerNetworks-UFRGS/scylla.git`
2. Follow the installation instructions in the provided documentation [TODO]
3. Execute **Scylla** during the boot time to enable automatic protection.

## Contributing

We welcome contributions from the community. If you find issues or have suggestions for improvements, please create an issue or submit a pull request.

## License

This project is licensed under the [Apache License 2.0](LICENSE) - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

We would like to express our gratitude to the open-source community and contributors for their valuable feedback and contributions to enhance **Scylla**.

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Language](https://img.shields.io/badge/Language-Python-green.svg)](https://www.python.org/)
[![Language](https://img.shields.io/badge/Made_with-eBPF-yellow.svg)](https://ebpf.io/)
