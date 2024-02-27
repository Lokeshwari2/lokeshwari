**By Referring to C-based Lab videos and RISC-V-based lab videos**

**Snapshots of the compiled C code and RISC-V**

**Step 1: check whether the leafpad is installed in ur machine by using the commands
leafpad sum1ton.c& (sum1ton.c is the file name)
If the leafpad editor is opened without any errors then type the C code.**
****If the leafpad is not installed in ur machine then install by using the following command**

**sudo snap install leafpad****

![WhatsApp Image 2024-02-26 at 11 30 38 PM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/05cca570-d4dd-46cb-b17e-6dbbbf12c364)

****Step 2: Writing the C code in the leafpad editor** using the following command

**leafpad sum1ton.c&**


**Step 3![WhatsApp Image 2024-02-26 at 11 30 34 PM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/3b719550-fde7-4940-97c7-fc97d3a9f7b1)
: After writing the C code save the editor by Ctrl+s**

**Step 4: Check for the errors by using the following command(compilation step)**

**gcc sum1ton.c**
![complie the C Code](https://github.com/Abdulbitm/Abdul/assets/160620896/982d5fe6-b150-4535-9611-8478a12165ae)

**Step 5: Check the output by using the command**

**./a.out**
![C Code Execution with results ](https://github.com/Abdulbitm/Abdul/assets/160620896/07457616-fb58-4bb1-9c1f-dd32f256625b)

**The results will be displayed as** 

**Sum of numbers from 1 to 500 is 125250**


********************************************************RISCV Compilation and Execution*****************************************************

**Step 1: View the C Code in the editor window using the following command**

**cat sum1ton.c**
![view in the C code in notepad](https://github.com/Abdulbitm/Abdul/assets/160620896/cd8e147a-6cf3-444d-a76c-1b24ed063636)

**Step 2: Compile the code in riscv using the following command**

**riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c**
![complie riscv](https://github.com/Abdulbitm/Abdul/assets/160620896/b85e4975-9bc1-4258-8091-6904692328cc)

**Step 3: The ls ltr command in Linux is used to list the contents of the current directory in long format, sorted by last modified time in reverse order.**

**use the command**

**ls -ltr sum1ton.c**

![view the directory contents](https://github.com/Abdulbitm/Abdul/assets/160620896/c7dd20be-b896-4d19-af98-077590a23b14)


![long directory content](https://github.com/Abdulbitm/Abdul/assets/160620896/3e2e473a-9f55-4bec-8ed3-4bd2732efbee)

**Search for the Main and check the instructions of the C code execution. It has 15 instructions in the C execution**

![checking instructions_in_main_C_Code_15_instructions](https://github.com/Abdulbitm/Abdul/assets/160620896/8d7d1502-a997-403d-a2cc-fcd459962a43)

![checking instructions_in_main_C_Code_15_instructions_highlighted](https://github.com/Abdulbitm/Abdul/assets/160620896/0a07ba3e-4a3d-41a7-a158-3ef976ce0292)


**Step 4:**

**riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c**

![12 instructions with Ofast](https://github.com/Abdulbitm/Abdul/assets/160620896/f2ebdc19-c3a6-494d-a25d-6d71c2811440)



![12 instructions with Ofast_1](https://github.com/Abdulbitm/Abdul/assets/160620896/4904feb4-c3ab-4337-976c-9a94bacbf85a)
