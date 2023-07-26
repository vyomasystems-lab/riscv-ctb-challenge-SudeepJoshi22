In Challenge1 Illegal .word 0 is written inside .text segment which caused the illegal instrucction exception to be raised.
![wrong](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level1/challenge3_illegal/level1_3_wrongcode.png)
In the trap handler, the mcause is compared with the CAUSE_ILLEGAL_INSTRUCTION which is a macro holding the value of 0x02. The code used to cause infinite loop because the trap handler used to return again to the same illegal instruction.
The illegal instruction again used to call trap handler and this would repeat indefinitely.
![fixed](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level1/challenge3_illegal/level1_3_correctedcode.png) 
I fixed it by making the trap handler return to the 2 instructions after the illegal instruction(j fail is skipped or else dump file will not be generated). 
The code ran successfully and dump file got generated.
