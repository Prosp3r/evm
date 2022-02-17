## Ethereum Virtual Machine(EVM)

### What it is and how it works.

The Ethereum Block Chain is made of a *"world state"* which is composed of Accounts with storage and in some cases code(refered to as smart contracts).

At the heart of this blockchain is the EVM. It accepts input data in the form of message calls, it processes these (commands in the message calls also refered to as *Opcodes*) along with the "current world" state to produce a state which then becomes the new current world state.

![EVM operation from a bird's eye view](/images/evm_birds_eye_view.png)


The EVM is a *(Quasi)Turing complete* 256 bit *stack based* virtual machine that allows anyone to execute arbitrary EVM byte code.
The EVM is actually a turin complete VM quasi is used to refer to the checks put in place to prevent infinit running codes being executed in the VM this is achieved using what's known as *Gas*


Definitions
World State


Stack - A first in first out data structure.