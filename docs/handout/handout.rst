Handout Materials
==================

We provide handout materials for the tutorial. It includes :ref:`environment setup instructions <environment setup>` and the :ref:`reading materials <reading materials>` for the frameworks to be introduced in the tutorial.

If you have any questions, especially about environment setup, please contact `Youwei Xiao (shallwe@pku.edu.cn) <mailto:shallwe@pku.edu.cn>`_. We will try our best to help you.

Environment Setup
^^^^^^^^^^^^^^^^^

We provide two setup methods for the involved frameworks: :ref:`Docker <docker>` and :ref:`local installation <local installation>`. We recommend using Docker to try out the frameworks.

Docker
"""""""""""""""""""""""""

Easiest way: use the built Docker image.
'''''''''''''''''''''''''''''''''''''''''


We provide a built Docker image for the tutorial. You can pull it from Docker Hub::

  docker pull uvxiao/ahs-tutorial:aspdac2025

Then, you can run the following command to start the container::

  docker run -it --rm uvxiao/ahs-tutorial:aspdac2025

The frameworks are installed inside the ``/root/repos`` directory.


Building Docker Image from Source
'''''''''''''''''''''''''''''''''''''''''


We also provide a repository for building the Docker image from source. Please refer to the `ahs-docker`_ repository for details. Here are some takeaways instructions::

  git clone git@github.com:pku-liang/ahs-docker.git
  cd ahs-docker
  # clone the framework collection
  git clone git@github.com:pku-liang/ahs-tutorial.git repos --recursive
  # make the run.sh executable
  chmod +x run.sh
  # pull the ubuntu images
  ./run.sh pull
  # build the base Docker image
  ./run.sh build -i ahs-docker
  # run a container with the frameworks mounted
  ./run.sh run -i ahs-docker -c ahs-docker -v mount.json
  docker attach ahs-docker
  # then inside the container:
  cd /root/repos
  chmod +x ./install.sh
  ./install.sh
  
.. _ahs-docker: https://github.com/pku-liang/ahs-docker

The produced Docker image should be the same as the ``uvxiao/ahs-tutorial:aspdac2025`` image.

Local Installation
"""""""""""""""""""""""""

We also provide a local installation script for the tutorial. Some prerequisites, including but not limited to Ninja, gperf, zip, are required, please refer to `Dockerfile`_ as a reference.

.. _Dockerfile: https://github.com/pku-liang/ahs-docker/blob/main/Dockerfile

Then, you can run the following commands to install the frameworks::

  git clone git@github.com:arch-of-shadow/ahs-tutorial.git
  cd ahs-tutorial
  git submodule update --init
  chmod 777 install.sh
  ./install.sh


Reading Materials
^^^^^^^^^^^^^^^^^

For every framework to be introduced in the tutorial, we provide its open-source repository link and related reading materials like publications, documentation, etc.

.. list-table::
   :header-rows: 1
   :widths: 20 30 50

   * - Framework
     - Repository
     - Materials
   * - POPA
     - `pku-liang/popa <https://github.com/pku-liang/popa/tree/mlir>`_
     - `FPGA'24 Paper(Lasa) <https://dl.acm.org/doi/10.1145/3626202.3637566>`_, `FCCM'23 Paper <https://ieeexplore.ieee.org/document/10171577>`_
   * - Hector
     - `pku-liang/Hector <https://github.com/pku-liang/Hector/tree/tutorial-aspdac>`_
     - `ICCAD'22 Paper <https://ieeexplore.ieee.org/document/10068908>`_
   * - Hestia
     - `pku-liang/hestia <https://github.com/pku-liang/hestia/tree/main>`_
     - `MICRO'24 Paper <https://ieeexplore.ieee.org/abstract/document/10764625>`_
   * - Cement
     - `pku-liang/Cement <https://github.com/pku-liang/Cement/tree/cmt2>`_
     - `FPGA'24 Paper <https://dl.acm.org/doi/10.1145/3626202.3637561>`_, `Crates.io Package <https://crates.io/crates/cmtrs>`_, `Documentation <https://docs.rs/cmtrs/latest/cmtrs/>`_
   * - OriGen
     - `pku-liang/OriGen <https://github.com/pku-liang/OriGen>`_
     - `ICCAD'24 Paper <https://arxiv.org/abs/2407.16237>`_, `Hugging Face <https://huggingface.co/henryen/OriGen>`_
   * - Khronos (ksim)
     - `pku-liang/ksim <https://github.com/pku-liang/ksim/tree/aspdac24-tutorial>`_
     - `MICRO'23 Paper <https://dl.acm.org/doi/10.1145/3613424.3614301>`_

Feel free to have a glance at the materials to get a sense of our works! We'll assist you to use them step-by-step in the tutorial.
