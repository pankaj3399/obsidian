![[Screenshot 2023-05-22 at 12.08.37 AM.png]]

![[Screenshot 2023-05-22 at 12.12.36 AM.png]]

calling a smart contract to get state doesn't require gas.
modifying state of network will need gas.
![[Screenshot 2023-05-22 at 12.24.24 AM.png]]

state -> number
RAM -> num

Calls are operations on smart contracts that do not result in a state change and typically only read data from the contract. Most calls are instant and do not require any gas. Anyone can make a smart contract call as these calls simply return data that is publicly available on the blockchain.

address data type - 20 bytes

map data structure is called mapping.It always returns some value, if the key is not present in map it will return the default value of the datatype.

![[abc.png]]


![[abc2.png]]

![[abc3.png]]

![[abc4.png]]

![[abc5.png]]

![[abc6.png]]

![[abc7.png]]

![[abc8.png]]

![[abc9.png]]

You can also use .transfer or .send to send ether in solidity.But be careful as we are providing control to other smart contracts when we deal with pay in solidity.

![[abc10.png]]

![[abc11.png]]

![[abc12.png]]

![[abc13.png]]

![[abc14.png]]

![[abc15.png]]

![[abc16.png]]

![[abc17.png]]

![[abc18.png]]

![[abc19.png]]


![[abc20.png]]

![[abc21.png]]


![[abc22.png]]

![[abc23.png]]

![[abc24.png]]

![[abc25.png]]

When you create a memory array from storage array it creates a copy.If from memory to memory then it creates an alias.
Multi dimension arrays are supported.Refer docs for more.

![[abc26.png]]

![[abc27.png]]

![[abc28.png]]

Loops use a lot more gas in solidity.
gasLeft() tells you how much gas is left.


