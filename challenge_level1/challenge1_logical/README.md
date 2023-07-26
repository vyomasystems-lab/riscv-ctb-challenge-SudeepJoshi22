Challenge1 Logical had 2 instructions written in the wrong way
![fix1](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level1/challenge1_logical/level1_fix1.png)
The source register-2 was written as "z4" which is not the correct name of the register define under RV32I. I changed it to "a4" which is the correct name of the register.
![fix2](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level1/challenge1_logical/level1_fix2.png)
andi instruction being the immediate instruction had 2 source registers deine here. The Immmediate instruction must define only one source register and one immediate value. I fixed it and defined a immediate value as 0x00f.
The make file ran successfully and generated the dump file.
