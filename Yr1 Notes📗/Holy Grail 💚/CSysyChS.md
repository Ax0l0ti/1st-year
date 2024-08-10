# Computer System Architecture Cheat Sheet
---
> [!info]+ Cheat Sheet Details
> Includes information about module, link to module and it's correspondent attribute tag 
> *Module Tag :* #CM12002 
> *Link :* [[Computer System Architecture]]
> *Cheat Sheet tag :* [[Grail 🩷]]]]
---
### Equations and phrases

**Structure :** (Topic) Phrase
#### Phrases
1. (Arch) von is flexing whilst Harvard in bed
2. (Pipelining) FD==**F**==ES 
3. (I/O) taking **Direct**  **DMA** on **Polls** **Interrupts** my **Memory** **Maps** & **Address** 
4. (Representation) **SEMB** Half **1 5 10 15** Single **1 8 23 127**  Full **1 11 52 1023** 
5. (Representation) ASCII 7 bits, ==**"A" = 65, "a" = 97**==
6. (Filesystem) Inode contains : Timestamps, Size, File type, Pointers, Aliases/Reference, privilege levels, 
#### Equations

$$ \text{Amdhal's law, N processors and p }= \%\text{tasks can be parellised . }  \frac{1}{(1-p)+\frac{p}{N}}$$

--- 
### Topics
#### Uniprocessor Architectures (von Neumann)
- Key words: von Neumann, uniprocessor, single instruction, single data, memory, CPU
#### Parallel Architectures
[[Yr1 Notes📗/Semester 1 & 2/Architecture/Architecture]]
- Key words: parallel, SIMD, MIMD, MISD, concurrency, multicore

##### Architecture types

| Architecture | Description                         | Example                              | Use Case                                  |
| ------------ | ----------------------------------- | ------------------------------------ | ----------------------------------------- |
| **SISD**     | Single instruction, single data     | Traditional PCs                      | General-purpose computing                 |
| **SIMD**     | Single instruction, multiple data   | GPUs, Vector Processors              | Image processing, scientific computing    |
| **MISD**     | Multiple instruction, single data   | Specialized fault-tolerant systems   | Fault tolerance, reliability verification |
| **MIMD**     | Multiple instruction, multiple data | Multi-core CPUs, Distributed Systems | Parallel computing, complex simulations   |
##### PU & Memory 
**Shared memory vs Individual Memory**
Shared
	Bad Scaling
	Requires cache Coherence 
	Memory to CPU bottleneck
	Atomic data
Individual 
	Scalar Scaling possible
	Inefficient communication
	Data Distribution is a pain in the ass

##### Solulu 

**Delulu ( Virtual shared memory )**
	Use virtual memory that is shared but acts as individual


##### Data Representation
[[Data Representation]]
- Key words: binary, hexadecimal, ASCII, floating point, signed integers, unsigned integers

Binary to Hex 
signed = 
##### Data Storage
[[Data Storage]]
- Key words: RAM, ROM, cache, registers, secondary storage, SSD, HDD

RAM - Random Access Memory,

Page, sheet, book 

###### Secondary Storage

|         | SSD                               | CD                 | HDD                                                             |
| ------- | --------------------------------- | ------------------ | --------------------------------------------------------------- |
| **Pos** | No moving parts<br>               | No moving parts    | +Storage                                                        |
| **Neg** | Limited number of **Read writes** | doesn't store much | Moving Parts, suspectable to corruption from vibrations e.g car |
##### Real Numbers
- **Key words**: floating point, IEEE 754, precision, exponent, mantissa, normalization
##### Representing and Executing Instructions
- **Key words**: opcode, operands, instruction set, fetch-decode-execute, machine code
##### Operand Modes and Instruction Set
- **Key words**: addressing modes, immediate, direct, indirect, register, instruction set architecture
#### Control and Pipelining
[[Pipelining]]
- **Key words**: control unit, pipeline stages, instruction pipeline, hazards, parallelism, throughput
#### Handling I/O, Programmed I/O
- Key words: input/output, I/O ports, memory-mapped I/O, polling, device drivers
##### Comparison of I/O Techniques

| Technique                              | Description                                    | Benefits                                           | Drawbacks                                                   |
| -------------------------------------- | ---------------------------------------------- | -------------------------------------------------- | ----------------------------------------------------------- |
| ==**Programmed**== I/O                 | CPU continuously polls device status           | Simple to implement, direct control                | Inefficient CPU usage, not suitable for high-speed devices  |
| ==**Interrupt-Driven**== I/O           | CPU is interrupted by device when ready        | Efficient CPU usage, suitable for multitasking     | More complex to implement, Reqs hardware & software support |
| ==**Direct Memory Access**== (**DMA**) | DMA controller handles data transfer           | Highly efficient for large transfers, frees CPU    | Additional hardware complexity, potential bus contention    |
| ==**Memory-Mapped**== I/O              | I/O devices assigned specific memory addresses | Simplifies I/O instruction set, uniform addressing | Complicates memory management, potential address conflicts  |
#### Interrupt/Direct Memory Access
- Key words: interrupt, DMA, ISR, priority, bus mastering, latency

#### Latches & Flip-Flops
[[Sequential Logic]]
**FLIPFLOP** takes **clock** as ==enabler==, **LATCH** **dis/enabled** at will this makes **flipflop** upd every ==clock cycle==
Everything is adaptions of $SR$ e.g $D$ is $SR$ but $R$ is $S'$, $JK$ is $SR$ 
##### Relationships and Usage

- **SR Latch**$\text{ Set Reset Latch}$:  Foundation of all other latches and flip-flops.
- **D Latch**$\text{ Data Latch}$: Simplifies SR latch by using a single data input.
- **D Flip-Flop** $\text{ Data FF}$ : Adds edge-triggered capability to D latch, used in ==synchronous== circuits.
- **JK Flip-Flop** $\text{ Jump Kick FF}$: ==Resolves SR== latch invalid state, adds versatility.
- **T Flip-Flop** $\text{ Toggle FF}$: Simplified JK flip-flop for ==toggling==, commonly used in counters.

| Flip-Flop/Latch  | Derived From | Inputs  | Operation                 |
| ---------------- | ------------ | ------- | ------------------------- |
| **SR Latch**     | -            | S, R    | Set, Reset, Hold, Invalid |
| **D Latch**      | SR Latch     | D, E    | Q follows D when E=1      |
| **D Flip-Flop**  | D Latch      | D, C    | Q follows D on clock edge |
| **JK Flip-Flop** | SR Latch     | J, K, C | Set, Reset, Toggle, Hold  |
| **T Flip-Flop**  | JK Flip-Flop | T, C    | Toggle Q on T=1           |

#### File Management 




### Other Stuff 

**Karnaugh graphs**  - Bool expression indicates grid index. x bits makes $2^x$ indexes
#### Protocols 

| Protocol   | Function                 | Key Characteristics                                                                          | Use Cases                                        |
| ---------- | ------------------------ | -------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| **TCP**    | Reliable communication   | Connection-oriented, error detection, flow control, congestion control, stream data transfer | Web browsing, email, file transfer               |
| **UDP**    | Unreliable communication | Connectionless, no guarantee of delivery/order, low overhead                                 | Video streaming, online gaming, VoIP             |
| **HTTP**   | Web communication        | Stateless, uses TCP, request-response model                                                  | Web pages, APIs                                  |
| **HTTPS**  | Secure web communication | HTTP over TLS/SSL, encrypted, secure                                                         | Secure web pages, secure APIs                    |
| **FTP**    | File transfer            | Uses TCP, supports authentication, directory operations                                      | File downloads/uploads                           |
| **SFTP**   | Secure file transfer     | FTP over SSH, encrypted, secure                                                              | Secure file transfers                            |
| **SMTP**   | Email transmission       | Uses TCP, transfers email between servers                                                    | Sending emails                                   |
| **IMAP**   | Email retrieval          | Uses TCP, access email on server, supports multiple folders                                  | Reading emails from server                       |
| **POP3**   | Email retrieval          | Uses TCP, downloads email from server                                                        | Downloading emails to local client               |
| **SSH**    | Secure remote access     | Encrypted, secure, uses TCP                                                                  | Remote login, command execution                  |
| **Telnet** | Remote access            | Unencrypted, uses TCP, command-line interface                                                | Remote login (less secure)                       |
| **DNS**    | Domain name resolution   | Converts domain names to IP addresses, uses UDP (and TCP)                                    | Browsing the web, network services               |
| **DHCP**   | Dynamic IP assignment    | Assigns IP addresses dynamically, uses UDP                                                   | Network configuration, IP management             |
| **SNMP**   | Network management       | Monitors network devices, uses UDP                                                           | Network monitoring, device management            |
| **NTP**    | Time synchronization     | Synchronizes clocks over network, uses UDP                                                   | Time-sensitive applications, network timekeeping |