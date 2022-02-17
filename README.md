## Ethereum Virtual Machine(EVM)

### What it is and how it works.

The Ethereum Block Chain is made of a *"WORLD STATE"* which is composed of Accounts with storage and in some cases code(refered to as smart contracts).

At the heart of this blockchain is the EVM. It accepts input data in the form of message calls, it processes these (commands in the message calls also refered to as *OPCODES*) along with the *"CURRENT WORLD STATE"* to produce a state which then becomes the new current world state.

![EVM operation from a bird's eye view](/images/evm_birds_eye_view.png)


The EVM is a *(Quasi)Turing complete* 256 bit *STACK BASED* virtual machine that allows anyone to execute arbitrary EVM byte code.

It is composed of several data components and a set of environment variables that are made available at execution time.

The EVM is actually a turing complete VM. Quasi is used due to the checks put in place to prevent infinit running codes being executed in the VM this is achieved using what's known as *GAS*



### Definitions
Below are clarification of some of the highlighted terms as they relate to the EVM. 
- Ethereum has two types of Accounts Externally owned accounts(controlled with private keys and without code) and Contract accounts with associated with a smart contract.
- Current World State referes to the most recent state of the ethereum blockchain after the most recent transactions are carried out.
- Stack Based - The EVM is built on a last-in first out data structure.
- GAS is the resource used as a means of compensation to the nodes that host the evm. Gas can be paid for with Wei, the smallest unit of ether(ETH) it's native currency for exchange. One wei is 10^18 Ethers.
- TURING COMPLETE means EVM can carry out any abitrary computation to completion
- OPCODES are the low level “human readable” instructions of the EVM. The EVM has 157 Opcodes in total 
    Some of these Opcodes require gas, others don’t. 

    Some opcodes have predefined gas cost(eg. ADD Opcode uses 3 gas). While others have dynamically computed gas cost(e.g CALL Opcode requires computation using formula specified in the yellow paper).




### OPCODES -> STACK

The EVM's 157 Opcodes total represent various combination of low level machine instructions in human readable form.

![General stack operation from a bird's eye view](/images/push_pop_stack.png)


## Stack Operations on the EVM
![EVM opcodes stack operation](/images/stack_ops.png)


### ADVANTAGES

- Simplicity of stack based structure.
- Small operations are Easier to assess.
- Easier to work with compared to register based VMs.
- 256-bit wordsize means larger range of hardware architectures even futuristic ones.
- Being a World computer means it's data set requires a lot more work to be maliciously manipulated.
- Issues like DDos is eliminated
- It's Turin completeness reduces the limits in reality of the EVM as long as there's enough Gas.
- 

### DISADVANTAGES
Because EVM operations are maintained through a stack, its operation efficiency is relatively low, and may take a long time to complete a complex operation.
Cost is typically uncertain to run operations on the EVM due to fluctuating Gas gas cost.


### PRECOMPILED CONTRACTS
Precompiled contracts are a compromise used in the EVM to provide more complex library functions that are not suitable for writing in opcode 
(usually used for complex operations such as encryption, hashing, etc.)

It also costs less for developers than using functions that run directly in the EVM


### EVM FLOW
![EVM opcodes stack operation](/images/evm-architecture.png)