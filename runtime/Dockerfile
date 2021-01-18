FROM centos:7
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

RUN yum -y update && \
    yum install -y epel-release && \
    yum install -y \
        ocl-icd \
	clinfo && \
    rm -rf /var/cache/yum/*

RUN mkdir -p /etc/OpenCL/vendors && \
    echo "libnvidia-opencl.so.1" > /etc/OpenCL/vendors/nvidia.icd

# nvidia-container-runtime
ENV NVIDIA_VISIBLE_DEVICES all
ENV NVIDIA_DRIVER_CAPABILITIES compute,utility
