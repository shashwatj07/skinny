# Construction

Number of rounds for SKINNY-n-t, with n-bit internal state and t-bit tweakey state.

<table>
    <thead>
        <tr>
            <th></th>
            <th colspan=3>Tweakey Size t</th>
        </tr>
		<tr>
            <th>Block Size n</th>
            <th>n</th>
	        <th>2n</th>
	        <th>3n</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>64</td>
            <td>32</td>
            <td>36</td>
		    <td>40</td>
	    </tr>
	    <tr>
            <td>128</td>
            <td>40</td>
            <td>48</td>
		    <td>56</td>
	    </tr>
    </tbody>
</table>

The SKINNY round function applies five different transformations: SubCells (SC), AddConstants (AC), AddRoundTweakey (ART), ShiftRows (SR) and MixColumns (MC).
![SKINNY Round](images/construction.jpg)

- [Tweakey Schedule](https://shashwatj07.github.io/skinny/construction/tweakeyschedule.html)
    - [Permutation](https://shashwatj07.github.io/skinny/construction/tweakeyschedule/permutation.html)
    - [LFSR](https://shashwatj07.github.io/skinny/construction/tweakeyschedule/lfsr.html)
- [SubCells (SC)](https://shashwatj07.github.io/skinny/construction/subcells.html): Depending on the block size, a 4-bit Sbox (for 64-bit block) or a 8-bit Sbox (for 128-bit block) is used.
- [AddConstants (AC)](https://shashwatj07.github.io/skinny/construction/addconstants.html): Some round-dependent constants are XORed to the first nibbles/bytes column of the cipher internal state.
- [AddRoundTweakey (ART)](https://shashwatj07.github.io/skinny/construction/addroundtweakey.html): Half a block is extracted from the tweakey state and XORed to the cipher internal state. The tweakey nibbles/bytes are permuted and updated with simple LFSRs.
- [ShiftRows (SR)](https://shashwatj07.github.io/skinny/construction/shiftrows.html): The nibbles/bytes of the cipher internal state are rotated to the right row-wise by some specified number of positions.
- [MixColumns (MC)](https://shashwatj07.github.io/skinny/construction/mixcolumns.html): Each nibbles/bytes column of the cipher internal state are multiplied by a binary matrix.
