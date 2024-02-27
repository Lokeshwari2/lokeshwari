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

![WhatsApp Image 2024-02-26 at 11 30 38 PM (1)](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/f4f2c218-bf2c-455a-9d79-f5e82efa4cd4)

**Step 5: Check the output by using the command**

**./a.out**

![WhatsApp Image 2024-02-26 at 11 30 38 PM (1)](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/ca7a2d03-2e57-49ba-8022-6a3de0c520e1)

**The results will be displayed as** 

**Sum of numbers from 1 to 500 is 125250**


********************************************************RISCV Compilation and Execution*****************************************************

**Step 1: View the C Code in the editor window using the following command**

**cat sum1ton.c**
![WhatsApp Image 2024-02-27 at 3 42 59 AM (1)](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/ba89846b-4829-4dfd-abef-f4c3adfa460d)

**Step 2: Compile the code in riscv using the following command**

**riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c**

![WhatsApp Image 2024-02-27 at 3 42 59 AM (1)](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/d1cef43e-e3f0-461d-9ad9-3456ac5d109d)

**Step 3: The ls ltr command in Linux is used to list the contents of the current directory in long format, sorted by last modified time in reverse order.**

**use the command**

**ls -ltr sum1ton.c**

![WhatsApp Image 2024-02-27 at 3 42 59 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/adb27cb3-b3da-4f4b-a56d-fc011c24cc66)

![WhatsApp Image 2024-02-27 at 4 00 28 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/05eccf13-9dda-4398-8df9-3fa204926507)

**Search for the Main and check the instructions of the C code execution. It has 15 instructions in the C execution**

![WhatsApp Image 2024-02-27 at 4 01 10 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/f7fb23f0-8ece-41e2-8a66-41052e094613)

![WhatsApp Image 2024-02-27 at 4 01 29 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/01f84c45-e59f-4c9b-89b8-d9ab28c5313a)

**Step 4:**

**riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c**

![WhatsApp Image 2024-02-27 at 4 01 54 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/80a34b25-8929-4d2f-88e5-90135ffd6417)

![WhatsApp Image 2024-02-27 at 4 02 14 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/ed237174-4cf4-48af-a946-ddb957c88119)


