Challenge2 Loop had a infinite loop condition occuring inside the which was not allowing the spike to generate the dump file.

![wrongcode](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level1/challenge2_loop/level1_2_wrongcode.png)
In the above code, values are taken from the data segment added and compared with the correct value. If the values are equal then it used to repeat for the next 3 memeory locations in the data segment.
The infinite loop was occuring due to the fact tha there was no termination condition. Even after checking the 3 data segments the to was getting incremented and again checking the correctness of the operation.
The operations used to come successful and beq was again goto loop due to the fact that .data segment is initialized with 0. So after the 0xcaff all the values were used to be zero and the result of addi used to come correctly.

![corrected](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level1/challenge2_loop/level1_2_corrected%20code.png)
I corrected the code by taking the end address where we wish to stop the code execution inside the t6 register. When t0 reaches that value it will jump to 'stop' and hence program execution is stoped.

![success](https://github.com/vyomasystems-lab/riscv-ctb-challenge-SudeepJoshi22/blob/main/challenge_level1/challenge2_loop/level1_2_complete.png)
Successfully generated the dump file.
