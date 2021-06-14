# container-engine-accelerators/nvidia-driver-installer/rhel

This directory contains the following files:

- `Dockerfile`
- `Makefile`
- `entrypoint.sh`
- `daemonset.yaml`

The first three files contain code for creating a docker container that can be
used to install NVIDIA GPU drivers. The `daemonset.yaml` file can be used to run
that docker container on a Kubernetes cluster. This was an experimental thing.
