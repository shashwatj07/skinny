# SKINNY
SKINNY is a lightweight SPN cipher that uses a compact Sbox, a new very sparse diffusion layer, and a new very light key schedule. Despite this, the construction manages to retain very strong security guarantees due to its carefully choosen components and their intricately defined interaction.

- [Construction](https://shashwatj07.github.io/skinny/construction.html)
	- [Tweakey Schedule](https://shashwatj07.github.io/skinny/construction/tweakeyschedule.html)
		- [Permutation](https://shashwatj07.github.io/skinny/construction/tweakeyschedule/permutation.html)
		- [LFSR](https://shashwatj07.github.io/skinny/construction/tweakeyschedule/lfsr.html)
	- [SubCells (SC)](https://shashwatj07.github.io/skinny/construction/subcells.html)
	- [AddConstants (AC)](https://shashwatj07.github.io/skinny/construction/addconstants.html)
	- [AddRoundTweakey (ART)](https://shashwatj07.github.io/skinny/construction/addroundtweakey.html)
	- [ShiftRows (SR)](https://shashwatj07.github.io/skinny/construction/shiftrows.html)
	- [MixColumns (MC)](https://shashwatj07.github.io/skinny/construction/mixcolumns.html)
- [SBox](https://shashwatj07.github.io/skinny/sbox.html)
	- [DDT](https://shashwatj07.github.io/skinny/sbox/DDT.html)
	- [LAT](https://shashwatj07.github.io/skinny/sbox/LAT.html)
	- [Analysis](https://shashwatj07.github.io/skinny/sbox/analysis.html)
