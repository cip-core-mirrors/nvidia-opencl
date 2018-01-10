ARG repository
FROM ${repository}:runtime-centos7
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

RUN yum install -y \
        ocl-icd-devel && \
    rm -rf /var/cache/yum/*
