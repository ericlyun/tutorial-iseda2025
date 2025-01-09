.. _setup_label:
Setup
=============

Docker
^^^^^^

We recommend using Docker to try out the frameworks.

**Using Built Docker Image**

We provide a built Docker image for the tutorial. You can pull it from Docker Hub::

  docker pull uvxiao/ahs-tutorial:aspdac2025

**Building Docker Image from Source**

You can refer to `ahs-docker`_ for instructions.

.. _ahs-docker: https://github.com/pku-liang/ahs-docker

**Local Installation**

We also provide a local installation script for the tutorial. Some prerequisites are required, please refer to `Dockerfile`_ as a reference.

.. _Dockerfile: https://github.com/pku-liang/ahs-docker/blob/main/Dockerfile

Then, you can run the following commands to install the frameworks::

  git clone git@github.com:arch-of-shadow/ahs-tutorial.git
  cd ahs-tutorial
  git submodule update --init
  bash install.sh
