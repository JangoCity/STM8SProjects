/** @page FLASH_WriteEraseBlockOnDataEepromMemory Write/Erase Block on data eeprom memory


  @par Example description

  This example provides a short description on how to use FLASH Write/Erase Block mode 
  on data eeprom memory and benefit for the Read While Write feature:
  - Program a block at a specified address (0x4000).
  - Check program block (Read byte).
  - Erase block using Erase block function.
  - Check erase (using Read byte).

  
  @par Directory contents

  - FLASH\FLASH_WriteEraseBlockOnDataEepromMemory\main.c                    Main file containing the "main" function
  - FLASH\FLASH_WriteEraseBlockOnDataEepromMemory\stm8s_conf.h              Library Configuration file
  - FLASH\FLASH_WriteEraseBlockOnDataEepromMemory\stm8s_it.c                Interrupt routines source (not used in this example)
  - FLASH\FLASH_WriteEraseBlockOnDataEepromMemory\stm8s_it.h                Interrupt routines declaration
  - FLASH\FLASH_WriteEraseBlockOnDataEepromMemory\stm8s208.lkf              STM8S208 and STM8S207 Linker file 
  - FLASH\FLASH_WriteEraseBlockOnDataEepromMemory\stm8s105.lkf              STM8S105 Linker file



  @par Hardware and Software environment

  - This example was developped to run on STM8S208 device with STMicroelectronics 
  STM8/128-EVAL evaluation board.
  
  - It can be tailored to run on any other supported device and developpement board.
  
  - This example has been tested with ST Visual Develop (STVD) toolchain
  (Cosmic compiler).

 
  @par How to use it ?

  In order to make the program work, you must do the following :
  - Create a project and setup all project configuration
  - Use the linker file given in the directory (stm8sxxx.lkf)
    -> In STVD Select Project\Settings\Linker\Category "input" then unchecks the "Auto" box 
       and in the "Script Lkf file name" field add the dedicated linker file.
    - When using the STM8S208 or STM8S207 device select the stm8s208.lkf linker file
    - When using the STM8S105 device select the stm8s105.lkf linker file

  - Uncomment the line "#define USE_COSMIC_SECTIONS  (1)" to use the cosmic section in the stm8s.h file.
  - Add the required Library files:
    - stm8s_flash.c
  - Edit stm8s.h file to select the device you are working on (#define STM8S208, in this case).

  @b Tip: You can tailor the provided project template to run this example, for more
          details please refer to "stm8s_fwlib_um.chm" user manual; select "Peripheral Examples"
          then follow the instructions provided in "How to proceed" section.  
   
  - With STVD ?
   - Rebuild all files: Build-> Rebuild all.     
   - Load project image: Debug->Start Debugging
   - Run program: Debug->Run (Ctrl+F5)

  - You can check the value of the bytes at the specified addresses by using the memory window in STVD.
  - The data read from the data memory is compared with the expected values.
  	The result of this comparison is stored in the "OperationStatus" variable.
   
  */

/******************* (C) COPYRIGHT 2009 STMicroelectronics *****END OF FILE****/
