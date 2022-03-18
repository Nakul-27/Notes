# User Datagram Protocol
Not Connection-Oriented

Fast, Unreliable, [[Packets]] not guaranteed to make it.

## UDP Segment Structure
4 Fields - *2 Bytes Each*
1. Source Port #
2. dest Port #
3. Length
4. Checksum
![[Pasted image 20220216221400.png]]

## Error Checking
### Checksum
Allows for Error checking.
**1 Bit Errors cannot get through but 2 bit errors could**.

#### Process:
1. Sender side performs the 1s complement of the sum of all the 16-bit words in the segment with any overflow being wrapped around.
2. Place (1) into the checksum section of the UDP Segment header
3. At the Receiver side, add all the 16-bit words in the segment and add the checksum. If the answer is all 1s then there is no error. 

