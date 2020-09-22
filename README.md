README
======

The C++ code follows the C++11 standard, tested with Visual Studio 2019. 
The RA requires the [NLOpt] library for non-linear optimization.
The MSFP and SG require the [BOOST] library for mathematical operations.

To mine the Frequent patterns from a sample, we use the fpgrowth.exe implemented by
Christian Borgelt, which is available from <https://borgelt.net/fpgrowth.html> and the
corresponding paper is [Borgelt].

The code has been tested on Windows 10. It may work also on other versions of Windows.
It was never tried on Linux.

Running
-------
####RA: 

Suppose the name of your VS2019 project is ProgSampRA, the usage of ProgSampRA.exe is

ProgSampRA minimum_support epsilon delta dataset

The output file is result.dat

For example: 
ProgSampRA 0.4 0.04 0.01 pumsb_star_rep1000.dat

####VC: 

Suppose the name of your VS2019 project is SampVC, the usage of SampVC.exe is

SampVC minimum_support epsilon delta dataset

The output file is result.dat

For example:
SampVC 0.4 0.01 0.01 pumsb_star_rep1000.dat

####MSFP: 

Suppose the name of your VS2019 project is msfp, the usage of msfp.exe is

msfp epsilon delta dataset minimum_support number_of_items

The output file is result_msfp.dat

For example:
msfp 0.04 0.01 pumsb_star_rep1000.dat 0.4 468

####SG: 

Suppose the name of your VS2019 project is sg, the usage of sg.exe is

sg epsilon delta dataset minimum_support number_of_items

The output file is result_sg.dat

For example:
sg 0.01 0.01 pumsb_star_rep1000.dat 0.4 468

Ensure that the fpgrowth.exe is in the same folder of ProgSampRA.exe, SampVC.exe, sg.exe or msfp.exe

[NLOpt]: https://nlopt.readthedocs.io/en/latest/ "NLopt homepage"
[BOOST]: https://www.boost.org/ "Boost homepage"
[Borgelt]: https://borgelt.net/papers/fpgrowth.pdf "An Implementation of the FP-growth Algorithm"
