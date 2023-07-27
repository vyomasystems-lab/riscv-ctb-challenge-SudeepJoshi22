In this challenge we see that, when we run make we get un-recognized opcode error. 
We can see that the insturctions are from the M-extention of RISC-V.
![error](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level2/challenge1_instructions/challenge_2_1_error.png)

In the rv32i.yaml we see that rv64: is set to 10. This means that 10% of the instructions generated will of the the type RV64M.
![problem1](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level2/challenge1_instructions/challenge_2_1_problem1.png)

But in the MakeFile we observe that the microarchitecture is given as rv32i for testing. These two problems are creating 'un-recognized opcode' error.

To fix this, I changed rv64m to rv32m in the .yaml file.
![fix2](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level2/challenge1_instructions/challenge2_1_fix2.png)

And in the MakeFile, I changed the microarchitecture to 'rv32im' which includes the insturctions of M-extention to my reference model.
![fix1](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level2/challenge1_instructions/challenge2_1_fix1.png)

The make ran successfully and generated the dump file.
![success](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level2/challenge1_instructions/challenge2_1_success.png)


