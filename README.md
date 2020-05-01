# VMG3926-B10A
reference repo for router configuration.

Unlock

Mac Address of LAN port // PASSWORD FOR ATEN

  ...0 or ...8 // 10F0A563
  
  ...1 OR ...9 // 887852B1
  
  ...2 OR ...A // C43C2958
  
  ...3 OR ...B // 621E14AC
  
  ...4 OR ...C // 310F0A56
  
  ...5 OR ...D // 1887852B
  
  ...6 OR ...E // 8C43C295
  
  ...7 OR ...F // C621E14A

(e.g. > ATEN 1, 1887852B)

Available commands:
ATMB                Use for multiboot.

ATHW                Other misc commands

ATDC                Disable Check Model Mechanism.

ATBB                Mark/unmark the Block X to be bad block.

ATCMP               Compare the contents at start address X and Y with L
                    ength Z
                    
ATLD                Download data with file name X to memory address Y f
                    rom PC via TFTP
                    
ATRB                Load the CFERAM to run by TFTP or UART!

ATDS                Dump data of spare area in block X`s page Y

ATRF                Read/Dump flash data

ATER                Erase NAND flash from block X to block Y

ATWF                Write data from RAM to flash

ATRT                Test memory.

ATCR                reset to default, erase Data partition

ATCD                Erase ROM-D partition

ATCM                Erase ROMFILE partition

ATWZ                write (a)MAC addr, (b)Country code, (c)EngDbgFlag, (
                    d)FeatureBit, (e)MAC Number to NVRAM
                    
ATCO                set Country Code to NVRAM.

ATSN                set Series Number to NVRAM.

ATSH                dump manufacturer related data from NVRAM

ATGO                Run program from flash image or from host depend on
                    [f/h] flag.
                    
ATSE                show the seed of password generator

ATEN                set BootExtension Debug Flag

ATBT                block0 write enable

ATPH                Set/Get PHY`s registers.

ATWW                Set memory or registers.

ATDU                Dump memory or registers.

ATBL                Print boot line and board parameter info

ATIP                Change booline parameters

ATAF                Change board AFE ID

ATBP                Change board parameters

ATSR                System reboot

ATUM                Upload ROMFILE to flash from TFTP

ATUD                Upload ROM-D to flash from TFTP

ATUB                Upload bootloader to flash from TFTP

ATUR                Upload router firmware to flash from TFTP

ATUW                Write the whole image start from beginning of the fl
                    ash from TFTP
                    
ATHE                print help

For more information about a command, enter 'athe command-name'

More information about each command:

CFE> athe atmb

  SUMMARY

     Use for multiboot.

  USAGE

     ATMB [a] (a=sec 0~60)

CFE> athe athw

  SUMMARY

     Other misc commands

  USAGE



CFE> athe atdc

  SUMMARY

     Disable Check Model Mechanism.

  USAGE

     ATDC

CFE> athe atbb

  SUMMARY

     Mark/unmark the Block X to be bad block.

  USAGE

     ATBB X Y
     X: block number
     Y: 1/0, Set/Unset.

CFE> athe atcmp

  SUMMARY

     Compare the contents at start address X and Y with Length Z

  USAGE

     ATCMP X Y Z
     X: src start address
     Y: dest start address
     Z: data length in dec.

CFE> athe atld

  SUMMARY

     Download data with file name X to memory address Y from PC via TFTP

  USAGE

     ATLD [hostip:]X [Y]
     X: file name. If 'UART', using UART
     Y: memory address, default using 0xffffffff

CFE> athe atrb

  SUMMARY

     Load the CFERAM to run by TFTP or UART!

  USAGE

     ATRB [[hostip:]X]X: file name. If NULL, using UART

CFE> athe atds

  SUMMARY

     Dump data of spare area in block X`s page Y

  USAGE

     ATDS X Y
     X: X`th block.
     Y: Y`th page.

CFE> athe atrf

  SUMMARY

     Read/Dump flash data

  USAGE

     ATRF a b [c]
     This command read the flash data to memory or
     directly dump the data on the screen.
     a: flash start offset address, b: length,
     c: specific ram address, type '0xffffffff' to use default or 'dump' to display

CFE> athe ater

  SUMMARY

     Erase NAND flash from block X to block Y

  USAGE

     ATER X Y
     X: start block #, Y: end block number.

CFE> athe atwf

  SUMMARY

     Write data from RAM to flash

  USAGE

     ATWF X Y Z
     X: RAM start address
     Y: flash offset address
     Z: data length in dec.

CFE> athe atrt

  SUMMARY

     Test memory.

  USAGE

     ATRT [options] addr length

     This command tests memory.  It is a very crude test, so don't
     rely on it for anything really important.  Addr and length are in hex

  OPTIONS

     -p:Address i (no information)
     -v:Address i (no information)
     -loop        Loop till key press

CFE> athe atcr

  SUMMARY

     reset to default, erase Data partition

  USAGE

     ATCR

CFE> athe atcd

  SUMMARY

     Erase ROM-D partition

  USAGE

     ATCD

CFE> athe atcm

  SUMMARY

     Erase ROMFILE partition

  USAGE

     ATCM

CFE> athe atwz

  SUMMARY

     write (a)MAC addr, (b)Country code, (c)EngDbgFlag, (d)FeatureBit, (e)MAC Number to NVRAM

  USAGE

     ATWZ a [b c d e]

CFE> athe atco

  SUMMARY

     set Country Code to NVRAM.

  USAGE

     ATCO X (X is country code)

CFE> athe atsn

  SUMMARY

     set Series Number to NVRAM.

  USAGE

     ATSN X (X = ASCII Serial Number with 13 bytes length)

CFE> athe atsh

  SUMMARY

     dump manufacturer related data from NVRAM

  USAGE

     ATSH

CFE> athe atgo

  SUMMARY

     Run program from flash image or from host depend on [f/h] flag.

  USAGE

     ex. ATGO [[hostip:]filenaem]
     if no filename, use the file name in 'Default host run file name'

CFE> athe atse

  SUMMARY

     show the seed of password generator

  USAGE

     ATSE X (X is project name)

CFE> athe aten

  SUMMARY

     set BootExtension Debug Flag

  USAGE

     ATEN X [Y] (Y=password)

CFE> athe atbt

  SUMMARY

     block0 write enable

  USAGE

     ATBT X (1=enable, other=disable)

CFE> athe atph

  SUMMARY

     Set/Get PHY`s registers.

  USAGE

     ATPH address_in_hex reg_in_hex [value_in_hex]

CFE> athe atww

  SUMMARY

     Set memory or registers.

  USAGE

     ATWW address_in_hex value_in_hex size_4_2_or_1

CFE> athe atdu

  SUMMARY

     Dump memory or registers.

  USAGE

     ATDU address_in_hex length_in_decimal

CFE> athe atbl

  SUMMARY

     Print boot line and board parameter info

  USAGE


CFE> athe atip

  SUMMARY

     Change booline parameters

  USAGE

     ATIP

CFE> athe ataf

  SUMMARY

     Change board AFE ID

  USAGE


CFE> athe atbp

  SUMMARY

     Change board parameters

  USAGE

     ATBP

CFE> athe atsr

  SUMMARY

     System reboot

  USAGE

     ATSR

CFE> athe atum

  SUMMARY

     Upload ROMFILE to flash from TFTP

  USAGE

     ATUM [hostip:]filename

CFE> athe atud

  SUMMARY

     Upload ROM-D to flash from TFTP

  USAGE

     ATUD [hostip:]filename

CFE> athe atub

  SUMMARY

     Upload bootloader to flash from TFTP

  USAGE

     ATUB [hostip:]filename [X]
     X: 1 to backup NVRAM, 0 to overwrite NVRAM.

CFE> athe atur

  SUMMARY

     Upload router firmware to flash from TFTP

  USAGE

     ATUR [hostip:]filename

CFE> athe atuw

  SUMMARY

     Write the whole image start from beginning of the flash from TFTP

  USAGE

     ATUW [hostip:]filename

CFE> athe athe

  SUMMARY

     print help

  USAGE

     ATHE [a] (a=command name)


     
 

