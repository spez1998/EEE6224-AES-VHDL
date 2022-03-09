# EEE6225-AES-VHDL
Group project implemeting low-area AES on FPGA

-------------------------------------------------------------
Ching Tung Chung
AES_shiftrow is the top level of the design

it include a look up table control and a 8 bit 25 register FIFO shifter

look up table control call LOOKUP_control
    (inv_LOOKUP_control use for decrypt)
shifter call c_shift_ram_0 con use in both encrypt and decrypt
  (if the file in the github can't use, please 
    1. find it from the IP catalog and search c_shift_ram / RAM-based Shift Register
    2. double click the IP sources
    3. choose
        variable length lossless
        resource
        only tick the register last bit
        width = 8
        depth = 25
    4. go to output (below component name)
        tick Clear(SCLR)
    )
-------------------------------------------------------------------------
