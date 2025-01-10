Cement instructions
-------------------

Introductions on the **cmtrs** embedded language, the **cmtc** compiler and some examples will be presented at the tutorial.

Please read the `documentation <https://docs.rs/cmtrs/latest/cmtrs/>`_ for the basic concepts and language usage.

Cement Example Contents
^^^^^^^^^^^^^^^^^^^^^^^

The examples are in ``Cement\crates\cmtc\examples`` directory.

We will demonstrate these examples
* ``fir.rs`` Finite Impulse Response filter. 

  * ``fn fir3_3()`` shows how to write an FIR with fixed length 3. 
  * ``fn gen_fir()`` shows how to generate FIR with arbitrary length.
  * ``fn gen_fir_addertree()`` further implements the FIR with an adder tree, which demonstrates the use of ``#[gen_fn]`` to generate hardware recursively.
  * ``fn make_tb()`` demonstrates how to write a testbench in ``cmtrs``.

* ``gemm.rs`` General Matrix Multiplication

  * ``fn mac()`` A multiply-accumulate unit to be used in the GeMM example.
  * ``fn gemm()`` A GeMM unit with only one MAC, which is controlled by a three-level for loop FSM. 
  * ``fn tb()`` A testbench for gemm.

* ``gemm_unrolled.rs`` Unrolled gemm

  * ``fn mac()`` A multiply-accumulate unit to be used in the GeMM example.
  * ``fn gemm_unrolled()`` A GeMM unit with ``#factor`` MACs, the innermost loop is unrolled and the memories are partitioned.
  * ``fn tb()`` A testbench for gemm_unrolled.

Running Cement Examples
^^^^^^^^^^^^^^^^^^^^^^^

Steps to run an example

.. code:: shell

    cd Cement
    cargo run -p cmtc --example <name_of_example>

Results:

* A generated System Verilog file at the root directory
* A Khronos simulation environment in ``tb`` directory

Simulation with Khronos
^^^^^^^^^^^^^^^^^^^^^^^

After running an example

.. code:: shell
  
    cd tb/<name_of_example>
    make all
    ./<executable_name>

Results:

* The executable will simulate the generated hardware, and prints the ``sim_print!`` messages in the testbench.


