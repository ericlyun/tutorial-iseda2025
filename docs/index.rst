
Agile Hardware Specialization: A toolbox for Agile Chip Front-end Design
=======================================================


.. note::
  **Important Updates!**
  
  2025/04/06: *Upload slides* `(1) lecture <rsrc/ahs.final.pdf>`_ `(2) hands-on <rsrc/hands-on.final.pdf>`_
   

Overview
--------

Compared to software design, hardware design is more expensive and time-consuming. This is partly because software community has developed a rich set of modern tools to help software programmers to get projects started and iterated easily and quickly. However, the tools are seriously antiquated and lacking for hardware design. Modern digital chips are still designed manually using hardware description language such as Verilog or VHDL, which requires low-level and tedious programming, debugging, and tuning. In this tutorial, we will introduce Agile Hardware Specialization (AHS) : A toolbox for Agile Chip Front-end Design. 

.. figure:: images/tutorial-overview.png
    :align: center
    :width: 450pt

The tutorial will highlight the methodology and open source tools in AHS for both chip design and verification. From the design perspective, AHS present two ways that use different programming interfaces and target different scenarios, including; 1) a multi-level hardware intermediate representation based high-level synthesis flow, which uses C and C++ as the programming language; 2) an embedded hardware description language, which uses Rust as the programming language. These two different methodologies exhibit different trade-offs in productivity and PPA (performance, power, and area) for chip design. From the verification perspective, we will present agile simulation and debugging tools, which can check the functional and performance behaviors of the hardware. The attendees will learn the methodology, design automation fundamentals, and software tools of AHS.

Setup
-----

We provide both Docker and local setup. See :ref:`Environment Setup<environment setup>` page for details.

Schedule
--------

The tutorial will be held at Monday, 31 March 2025 (11:00 CEST - 12:30 CEST). 

Detailed Program
"""""""""""

* Part 1: Lecture (1 hour), slide: `lecture <rsrc/ahs.final.pdf>`_ 
* Part 2: Hands-on session (30 mins), slide: `hands-on <rsrc/hands-on.final.pdf>`_
  

Repos and Publications
------------------------

.. list-table::
   :header-rows: 1
   :widths: 20 30 50

   * - Framework
     - Repository
     - Materials
   * - POPA
     - `pku-liang/popa <https://github.com/pku-liang/popa/tree/mlir>`_
     - `FPGA'24 Paper <https://dl.acm.org/doi/10.1145/3626202.3637566>`_, `FCCM'23 Paper <https://ieeexplore.ieee.org/document/10171577>`_
   * - Hector
     - `pku-liang/Hector <https://github.com/pku-liang/Hector/tree/tutorial-aspdac>`_
     - `ICCAD'22 Paper <https://ieeexplore.ieee.org/document/10068908>`_
   * - Hestia
     - `pku-liang/hestia <https://github.com/pku-liang/hestia/tree/main>`_
     - `MICRO'24 Paper <https://ieeexplore.ieee.org/abstract/document/10764625>`_
   * - Cement
     - `pku-liang/Cement <https://github.com/pku-liang/Cement/tree/cmt2>`_
     - `FPGA'24 Paper <https://dl.acm.org/doi/10.1145/3626202.3637561>`_, `Crates.io Package <https://crates.io/crates/cmtrs>`_, `Documentation <https://docs.rs/cmtrs/latest/cmtrs/>`_
   * - Khronos (ksim)
     - `pku-liang/ksim <https://github.com/pku-liang/ksim/tree/aspdac24-tutorial>`_
     - `MICRO'23 Paper <https://dl.acm.org/doi/10.1145/3613424.3614301>`_



.. toctree::
   :maxdepth: 3
   :caption: Contents:

   handout/index

   instructions/index
