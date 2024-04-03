### Stack machine EVM

- Where can we store data in contract and evm. Once transient storage comes in.

- EVM work with and keep track of like stack , memory, storage. These three we will be looking at.

- computation in contract where we want to compute the EVM data and where we want to store it?

- EVM is known as Stack machine and cheapest place to do all operation is known as stack.

- mingas of Stack is low. like for example the add operation opcode uses stack to add two numbers which cost 3 gas.

- literally it is a stack. like first come and last out system.

- memory ?
- unlike stack where you put one data inside at a time and the next one will at final index and to use it you may need to put last one out and then use index zero. But in memory you can stick it at any place you want. But at tne end of the transaction every thing is cleared afterwards. It is similar to stack cost 3 gas using mstore opcode.

- storage?
- It works like the same as memory but we can stick data in a giant array where ever we want and when ever we want but at the end of transaction it still persist. It is gas expensive like the sstore opcode which storgae information cost 100 gas.

- these are minimum gas fees.
- most computation and operation on the stack needs to be done.

## Push and Add OPCode Example:

- when ever adding data to stack we need to use push opcode and there are number of many push opcodes and after the push the number represent the no of bytes code we need to send after the bytecode. Not including push0 which only push 0 in the stack.

- But when push code 1 opcode(push1) we send with data 0x01 =1

- then again push1 which is push1--> 0x03=3 then 3 on top of stack and below is 1.

- then if we use add opcode which will look at top of the stack and underneath that stack value. then it adds 3+1 and the resulting value is 4. like getting the data out of stack and then add it and then push it. It use LIFO method ( last in and first out). after add worsk it will show only added value not others. this is push and Add opcode. push send stuff in the stack and add combines the last 2 and push it.
