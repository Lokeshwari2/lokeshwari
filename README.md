# lokeshwari
# A 4-week Research Internship on RISC-V using VSDSquadron Mini RISC-V Dev Board



BOARD SPECS:

| CH32V003F4U6 chip with 32-bit RISC-V core based on RV32EC instruction set |
| ------------------------------------------------------------------------- 
| SRAM                                                                       2kb onchip volatile sram     16kb external program memory                                    |
| Processor                                                                  24 MHz                                                                                       |
| Sink Current per I/O Pin                                                   8 mA                                                                                         |
| Source Current per I/O Pin                                                 8 mA                                                                                         |
| Input voltage (nominal)                                                    5 V                                                                                          |
| I/O voltage                                                                3.3 V                                                                                        |
| Programmer/debugger                                                        Onboard RISC-V programmer/debugger, USB to TTL serial port support                           |
| SPI                                                                        1x, PC5(SCK), PC1(NSS), PC6(MOSI), PC7(MISO)                                                 |
| I2C                                                                        1x, PC1(SDA), PC2(SCL)                                                                       |
| USART                                                                      1x, PD6(RX), PD5(TX)                                                                         |
| External interrupts                                                        8 external interrupt edge detectors, but it only maps one external interrupt to 18 I/O ports |
| PWM pins                                                                   14X                                                                                          |
| Analog I/O pins                                                            10-bit ADC, PD0-PD7, PA1, PA2, PC4                                                           |
| Digital I/O pins                                                           15                                                                                           |
| Built-in LED Pin                                                           1X onboard user led (PD6)                                                                    |
| USB 2.0 Type-C                                                            
   

This repo is intended to document the weekly progress.

### The first online meet was held on 16th of Feb 2024 @6PM

<details>
    <summary> TASK 1 - INSTALLING TOOLS</summary>

1) install RISC-V GNU Toolchain 

2) install Yosys 

3) install iverilog 

4) install gtkwave

### CLONING RISC-V GNU TOOLCHAIN

```sudo apt install git-all```   # To install git

```sudo apt-get install autoconf automake autotools-dev curl python3 libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev``` *make sure to install the dependencies*

![WhatsApp Image 2024-02-23 at 2 09 41 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/328abec4-b19b-4649-a449-85793253baf6)


```git clone https://github.com/riscv/riscv-gnu-toolchain```

![WhatsApp Image 2024-02-23 at 2 09 47 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/fc2974bd-7a56-4842-bca7-86fc5cb5fcbd)


## Create a opt dir
```mkdir /opt/riscv```  *try sudo incase of permission denial*

In my case I created a driectory ```mkdir riscv``` and ``` chmod 777 home/nawras/riscv ```

## Config and make inside the risc-v gnu toolchain dir 

```./configure --prefix=/opt/riscv```  

In my case ```./configure --prefix=/home/nawras/riscv```  

Then
```make``` **(Have patience)**

### Troubleshooting

**ERROR 1**: "gcc not found"
try ```sudo apt-get install build-essential```
see if gcc is in /usr/bin/

**ERROR 2**: "no acceptable c compiler found in $PATH"
Open the .bashrc by any editors like vim,emacs,nano,gedit ```nano ~/.bashrc``` 
Add the below line at the end of .bashrc and save it
```export PATH="$PATH:/usr/bin/gcc```

**ERROR 3**: Even after installing gcc g++ sometimes it shows 'gcc' command not found ,though it suggest to ```sudo apt install gcc``` which again will cause the same error. I figured this by ```ls```'ing the /usr/bin directory to find the gcc g++ cc to be in red text with black background indicates broken link or missing file.


Better purge it at **YOUR OWN RISK** and reinstall it again.
```sudo apt-get purge gcc```

or **REINSTALL** ```sudo apt-get install --reinstall gcc``` (didn't work for me)



### INSTALLING IVERILOG GTKWAVE & YOSYS

### YOSYS

```bash
git clone https://github.com/YosysHQ/yosys.git
cd yosys 
sudo apt-get install build-essential clang bison flex \libreadline-dev gawk tcl-dev libffi-dev git \ graphviz xdot pkg-config python3 libboost-system-dev\libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make 
sudo make install
```
![WhatsApp Image 2024-02-23 at 2 09 47 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/f908b9e2-63d1-47d9-9ae7-deb1ae2f9bd5)



![WhatsApp Image 2024-02-23 at 2 09 51 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/0797e38d-9a49-4158-9f1c-d9a598949bdb)


### iVerilog

```
sudo apt-get install iverilog
```
![WhatsApp Image 2024-02-23 at 2 09 52 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/4d06636d-f20e-438a-a9eb-8ef16220aef5)


### GTkWave
``` sudo apt-get install gtkwave ```


![WhatsApp Image 2024-02-23 at 2 09 57 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/0c21b5c3-4338-4a42-adde-ba9849c83ac6)


 


    
   
</details>
