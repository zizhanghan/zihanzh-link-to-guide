# zihanzh-link-to-guide
machine environment   
  Os: ubuntu-22.04.1-desktop-amd64  
  Processor: intel i5-7300HQ <br>
  Equipment name: LAPTOP-1HPTGCOF <br>
  
Install software<br>
  1 Terminal<br>
  Because the Ubantu os is a linux os, it contains a terminal. We can open the document and right click to open the terminal.
  
  2 Vim/txt editor<br>
    one: we can use the command "gedit" to open the txt.<br>
    two: we can use the vim to open the txt. My habit is using the gvim. However, the ubantu is not equipped the gvim editor. We should install the gvim. <br>
		Let's follow the operation below.<br>
		install ppa<br>
		![image](https://user-images.githubusercontent.com/114272466/195966116-140427f8-3edd-4b27-b48d-f2fe3f18c315.png)<br>
		Update<br>
		![image](https://user-images.githubusercontent.com/114272466/195966127-bfa7684c-2e1b-43c4-8644-3eb3c93c722b.png)<br>
		Install vim<br>
		![image](https://user-images.githubusercontent.com/114272466/195966262-636f04c7-e56a-4721-8674-d0fb50c05238.png)<br>
		Install gvim<br>
		![image](https://user-images.githubusercontent.com/114272466/195966277-17c0165b-002e-47cd-9d6a-0f74839a09f9.png)<br>
		shutdown<br>
		![image](https://user-images.githubusercontent.com/114272466/195966290-19e0cbc3-13c2-4d0b-a832-db401e011680.png)<br>



  3 Serial console<br>
    Install screen using sudo apt install screen. Then, I use "sudo screen /dev/ttyACM0" to connect serial console.
    
  4 Git<br>
    Use sudo apt install git to install git so that you could clone the repos from the github
  
  5 Cmake & GNU Embedded Toolchain for ARM<br>
    Use sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build essential to install all Cmake&GNU toolchain for ARM
    
    
Guide from 0 to Hello world<br>
  1. Quick pico setup<br>
    ![image](https://user-images.githubusercontent.com/114272466/195963560-dccaa5b0-eb33-45a1-8472-f5650a8d7cd9.png)
    ![image](https://user-images.githubusercontent.com/114272466/195963567-9b24f049-30a1-44fc-8f72-1f8c1a50b187.png)
    ![image](https://user-images.githubusercontent.com/114272466/195963584-b7d1d624-d77a-4f2a-a51b-321ae49a8010.png)

    These commands help me do:
    .Create a directory called pico
    .Install required dependencies
    .Download the pico-examples... repositories
    .Define the pico-examples... path in ~/.bashrc
    .Build blink and hello world examples in pico_examples file
    .Download and build picotool
    .Download and install Visual Studio Code.
    
  2. Install the toolchain<br>
    .Use the following code to install the toolchain for ARM<br>
    ![image](https://user-images.githubusercontent.com/114272466/195963691-780a2e44-2531-4cda-9bb8-3ded2c0dfa05.png)<br>

     .Because I use Ubuntu, I need to also install libstdc++-arm-none-eabi-newlib by using "sudo apt install libstdc++-arm-none-eabi-newlib".<br>
		 If you have intall the libstdc, the os will inform you without deleting anything.
    
  3. Show Hello world<br>
    First: See the hello world code in the /pico/pico_examples/hello_world/usb/hello_world.c<br>
    ![image](https://user-images.githubusercontent.com/114272466/195963917-fe8bff5b-8eba-458d-8c93-e91c67c12702.png)
    	
  Second: Build Hello World<br>
      Use the command: cd hello_world / make -j4. j4 means that the building will be processed in parallel by 4 processors.<br>      

  Third: Connect the RP2040 to the OS.<br>
      Make sure that you hold down the  BOOTSEL button to force it into USB Mass Storage Mode. holding down the boot button is really important.<br>
      Holding down the boot button is really important. Then, connect the RP2040 to the OS. It will ocurr the file called RP1_RP2. After that, <br>
      Drag the hello_world.uf2 to the file RP1_RP2
         
  Finally: open serial console<br>
      ![image](https://user-images.githubusercontent.com/114272466/195966372-7135dec2-523b-40b1-b2d2-857a28ba0c8a.png)<br>
      Now, you should be able to see the printed "hello world!" in your terminal window. Congratulations!
      
      
    
    
    
    
    
    
    
    
    
    
    
    
  
      
  
