A 6-bit affine LFSR, whose state is denoted (rc5, rc4, rc3, rc2, rc1, rc0)
(with rc0 being the least significant bit), is used to generate round constants. Its update
function is defined as<br />
![update function of the LFSR used in generating round constant](../images/lfsrroundconstant.jpg)

The six bits are initialized 0 and are updated before use in a given round <br />
## Table for round constants for each round
<!-- |  Round |1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62
| :---:  |
|constant| -->
| Rounds |Constants|
| :---:  |  :---:  |
| 1 -16 | 01,03,07,0F,1F,3E,3D,3B,37,2F,1E,3C,39,33,27,0E |
|17 - 32| 1D,3A,35,2B,16,2C,18,30,21,02,05,0B,17,2E,1C,38 |
|33 - 48| 31,23,06,0D,1B,36,2D,1A,34,29,12,24,08,11,22,04 |
|49 - 62|   09,13,26,0C,19,32,25,0A,15,2A,14,28,10,20     |


Then bits are arranged in a array of 4x4. depending on the size of bits in a cell of state matrix as shown in the below diagrams.
### For s = 4
![4x4 array from the affine 6 bits](../images/arrayformationfor4.jpg)

### For s = 8
![4x4 array from the affine 6 bits](../images/arrayformationfor8.jpg)


The round constants are combined with the state, respecting array positioning, using
bitwise exclusive-or

![XOR with round constant](..\images\xorwithroundconstant.jpg)

