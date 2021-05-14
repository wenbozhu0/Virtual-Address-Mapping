# Virtual-Address-Mapping

Read information about an existing Translation Lookaside Buffer (TLB), the Virtual Address Page table, and Physical Memory Direct Memory cacing.
Based on storing this information, your program will prompt the user a virtual address (in hex) and output the byte at that location.
Your program may als print out "Can not be determined", if the data is not available.
The first part of your program will be to read in 3 types of data - TLB, Page Table and Physical Memory Cache
A format sample is below:

```
Format of Record Type 2: TLB Contents
TLB,Set index, Tag, PPN
Examples
TLB,0,09,0D   - this means the TLB holds PPN 0D at set index 0 with a tag of 09
TLB,0,07,02   - this means the TLB holds VPN 02 at set index 0 with a tag of 07
```
Format of Record Type 2: Virtual Page Table
Page, Virtual Page Number, Physical Page Number
Examples:
Page,0,28
Page,2,33
Page,3,02

Format of Record Type 3: Physical Page Cache
Cache,Cache Index,Tag,ByteOffset0, ByteOffset1,ByteOffset2, ByteOffet3
Cache,0,19,99,11,23,11
Cache,2,1B,02,04,06,08
Cache,4,32,43,6D,8F,09
Cache,5,0D,36,72,F0,1D

Format of Record Type 4:  DONE
DONE
Indicates no more input of the TLB, Page Table or Cache. It is now time to prompt the user for a Virtual Address and output the byte (or can not be determined) at that location.

3 Times do the following;
Print out "Enter Virtual Address:", then input the Virtual Address in Hex
Output the byte found in Hex, or " Can not be determined"
