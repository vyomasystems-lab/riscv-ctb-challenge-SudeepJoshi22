Errors found by running randomized test.

1) Generating 100 instructions with all the instructions as compute.
Error addresses:
![address](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level3/error%20addresses.png)

Assembly lines corresponding to the addresses:
![err1](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level3/error1.png)
![err2](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level3/error2.png)
![err3](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level3/error3.png)

This indicates that there is the error in OR, and ORI instruction in the riscv_buggy design.

2) When higher number of instructions are included in the AAPG generation, also different classes of instructions are included, erros are found to for SRL, SRLI, and LW. Instruction but not all. This indicates that there is only error with OR, ORI and
3) due the wrong value stored in the register by OR and ORI instructions is reflected by there instructions giving wrong values.
   My findings can be found in the PDF file below.
   
