## Ethereum Virtual Machine(EVM)
*What it is and how it works.*


The EVM is a (Quasi)Turing complete 256 bit stack based virtual machine that allows anyone to execute arbitrary EVM byte code.


The Ethereum Block Chain is made of a "world state" which is composed of Accounts with storage and in some cases code( refered to as contracts).

At the heart of this blockchain is the EVM, it accepts input data in the form of message calls processes it(commands in the message calls also refered to as Opcodes) along with the "current world" state to produce a state which then becomes the new current world state.

Stack - A first in first out data structure.