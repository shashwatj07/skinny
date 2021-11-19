# AddRoundTweakey
The first and second rows of all tweakey arrays are extracted and
bitwise exclusive-ored to the cipher internal state, respecting the array positioning. <br />
### Flow chart for this operation
![addroundtweakeystep for first row](../images/addtweakey.jpg)
<br />
Do the same with the second row from the state matrix and tweakeys.
