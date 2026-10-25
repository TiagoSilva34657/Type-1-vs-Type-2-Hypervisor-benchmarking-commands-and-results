# Type 1 vs Type 2 Hypervisors: Benchmarking

Group project comparing the performance of a **Type 1** hypervisor (Proxmox VE) and a **Type 2** hypervisor (Oracle VirtualBox) in terms of CPU, memory, disk I/O and network.


## Test environment

| | Type 1 | Type 2 |
|---|---|---|
| Hypervisor | Proxmox VE | Oracle VirtualBox |
| Guest OS | Ubuntu Server | Ubuntu Server |
| RAM | 8192 MB | 8192 MB |
| vCPUs | 4 | 4 |
| Disk | 32 GB | 32 GB |

## Benchmark tools

| Resource | Tool |
|---|---|
| Disk / file system | IOzone |
| Memory | RAMspeed |
| Network | iPerf3 |
| CPU | Geekbench 7 |

## Repository contents

- `Comandos para Testes.txt`: how to install each tool and the exact commands we used, plus the network setup needed for the iPerf3 tests (including the difficulties we had connecting the Type 1 hypervisor).
- `finaltests/`: the results of all the benchmarking tests, separated into `type1/` and `type2/` subfolders.

## How to reproduce

1. Create a VM with the same specs on each hypervisor (see table above) and install Ubuntu Server.
2. Follow `Comandos para Testes.txt`, section 0 (VM preparation) and then the installation steps for each tool.
3. For the iPerf3 tests, set up the network as described in section 3.1 of the guide.
4. Run the commands from each section on both VMs, keeping the same conditions (same VM settings, no other applications running), and compare the results.

## Authors

Tiago Valente M16814 - Ticiano Chendo M16894 - Ruben Sampaio E12013 - Tiago Silva M16346
