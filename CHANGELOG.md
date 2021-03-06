Version 2.0 -- 2019-04-08
-------------------------

* Implement Picnic 2.
* Use 4-times parallel SHAKE3 for faster PRF evaluation, commitment generation, etc.
* Fix size of salts to 32 bytes.

Version 1.3.1 -- 2018-12-21
---------------------------

* Reduce heap usage.

Version 1.3 -- 2018-12-21
-------------------------

* Implement linear layer optimizations to speed up LowMC evaluations. Besides the runtime improvements, this optimization also greatly reduces the memory size of the LowMC instances.
* Provide LowMC instances with m=1 to demonstrate feasibility of those instances.
* Sligthly improve internal storage of matrices to require less memory.
* Remove unused code and support for dynamic LowMC instances.

Version 1.2 -- 2018-12-05
-------------------------

* Implement RRKC optimizations for round constants.
* Compatibility fixes for Mac OS X.
* Reduce memory usage when using Fiat-Shamir and Unruh transform in the same process.
* Fix deviations from specification. The KDF was missing the output length as input and the public key was incorrectly serialized. Note that this change requires an update of the test vectors.
* Update SHA3 implementation and fix endiannes bug on big-endian.
* Record state before Sbox evaluation and drop one branch of XOR computations. This optimization is based based on an idea by Markus Schofnegger.
* Add per-signature salt to random tapes generation. Prevents a seed-guessing attack reported by Itai Dinur.

Version 1.1 -- 2018-06-29
-------------------------

* Compatibility fixes for Visual Studio, clang and MinGW.
* Various improvements to the SIMD versions of the matrix operations.
* Default to constant-time matrix multiplication algorithms without lookup tables.
* Add option to feed extra randomness to initial seed expansion to counter fault attacks.
* Version submitted for inclusion in SUPERCOP.

Version 1.0 -- 2017-11-28
-------------------------

* Initial release.
* Version submitted to the NIST PQC project.
