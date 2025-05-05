## 原因
keil5此前已被破解过，相当于在已安装ARM工具链的Keil环境下安装51单片机工具链。
## 解决
- 在TOOLS文件中添加如下代码
![11](https://github.com/user-attachments/assets/2b5582fc-8d05-48ab-850d-8fb004be8bab)
```C
[C51]
PATH="d:\Keil_v5\C51\" //换成你的路径\"
VERSION=V9.56          //换成你的版本
BOOK0=HLP\Release_Notes.htm("Release Notes",GEN)
BOOK1=HLP\C51TOOLS.chm("Complete User's Guide Selection",C)
TDRV0=BIN\MON51.DLL ("Keil Monitor-51 Driver")
TDRV1=BIN\ISD51.DLL ("Keil ISD51 In-System Debugger")
TDRV2=BIN\MON390.DLL ("MON390: Dallas Contiguous Mode")
TDRV3=BIN\LPC2EMP.DLL ("LPC900 EPM Emulator/Programmer")
TDRV4=BIN\UL2UPSD.DLL ("ST-uPSD ULINK Driver")
TDRV5=BIN\UL2XC800.DLL ("Infineon XC800 ULINK Driver")
TDRV6=BIN\MONADI.DLL ("ADI Monitor Driver")
TDRV7=BIN\DAS2XC800.DLL ("Infineon DAS Client for XC800")
TDRV8=BIN\UL2LPC9.DLL ("NXP LPC95x ULINK Driver")
TDRV9=BIN\JLinkEFM8.dll ("J-Link / J-Trace EFM8 Driver")
RTOS0=Dummy.DLL("Dummy")
RTOS1=RTXTINY.DLL ("RTX-51 Tiny")
RTOS2=RTX51.DLL ("RTX-51 Full")
LIC0=03LZX-HY1VP-5GZ7V-PZWTF-QF686-RNIQW
```
