# Input Output
---
> [!info]+ File Details
> Includes information about when file was created, what module the note belongs to. **Some** notes have listed teachers and Resources.
> > *Date :*  28-11-2023 
> > *Module :* #CM12002 
> > *Teacher*: #FabioNemetz 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#External devices]]
> [[#I/O modules Functions]]
> [[#Control of I/O devices]]
> [[#Memory-Mapping of I/O]]
> [[#Device Flags]]
> [[#Handling Input / Output]]
> [[#DMA Direct Memory Access]]
> 
--- 

Any transfer of information beyond the CPU and main memory is considered to be I/O e.g. disk storage. 

A computer architecture needs to specify how data is sent out and recieved and how to manage requests for input and outputs particularly for devices with differnt requirements and capabilities. 

One of the important variable in I/O devices is their operating speed. This can be in the form of:
	- **Electronics** (other computers)
	- **Electromechanical** (printer, disk)
	- **Human** (mouse, keyboard)

### External devices
External devices provide a means of exchanging data between the external environment and the computer. They attach to the computer by a link to an I/O module.

External devices can be categorized in three parts:
•**Human readable**
	Suitable for communicating with the computer user
	Video display terminals (VDTs), printers
•**Machine readable**
	Suitable for communicating with equipment
	Disk and tape systems, sensors and actuators
•**Communication**
	Suitable for communicating with remote devices such as a terminal, a machine-readable device, or another computer

### I/O modules: Functions
- Control and timing
- Processor communication
- Device communication
- Data buffering 
- Error detection

Three techniques are possible for I/O operations:
- **Programmed I/O**
	- Processor executes a program that gives it direct control of the I/O operations. This means that the processor must wait until the I/O operation is complete. This wastes processor time as processors are generally faster than I/O module. 
- **Interrupt-drive I/O**
	- Processor issues an I/O command and continues to execute other instruction. The processor is interrupted by the I/O when the first process is completed. 
- **Direct memory access (DMA)**
	- The I/O module and main memory exchange data directly without processor involvement. 

![[Interrupt Types.png]]

### Control of I/O devices

##### Single Device Control
- A stored I/O operation instruction is fetched to the IR in the CPU
- An instruction from the control unit to the I/O control unit causes the I/O control unit to send signals to the device to set it into action. 
- Data will need to be transferred to the device (a write) or from the device (a read). The data is stored in a data register
![[Control of Device IO.png| 400]]

##### Multi-Device Control
The above is for a single device. However, there may be several devices. So the I/O instructions must be structured and coded into a bit pattern with three parts that describe: 
- An I/O operation code;
- The direction of transfer (read/write)
- The address of the device

The supporting hardware for multiple device control is assigned as such:
	- I/O data place on a common I/O data bus
	- The address information can also be placed on a common I/O address bus
![[Control of Multi Device IO.png| 400]]

**Advantages** of having a shared I/O bus are:
	- Simplicity and flexibility $\to$ a single I/O control system with a single connection to the CPU. 
**Disadvantages** are: 
	- Cost of building a shared bus
	- The possibility of contention for the shared resources of the bus. 

### Memory-Mapping of I/O
Many architectures connect the CPU to the store unit by a single bus. The number of locations that can be accessed are determined by the number of bits in the address lines of the bus. So if the bus had 24 lines then we can address $2^{24}$ locations. This is the address space of such a machine. This is **memory-mapping** of I/O. 

![[Memory Mapping of IO.png| 400]]
This arrangement allows data to be transmitted along the data lines of the bus, address along the address lines and read/write inforamtion along the control lines. 

Advantages of memory-mapping
	- Simplifies I/O control, freeing CPU space for other uses

Disadvantages of memory-mapped I/O
	- Uses of address space, which then can't be used for storage
	- I/O devices are in contention with the store for the same bus
	- Programs may be harder to understand as I/O storage can be confused

The I/O we have been talking about is called programmed I/O because it is the programmer who writes code to access data transfer it to for from devices. 

### Device Flags
- Each device has a register that contains a one-bit register which acts as a device status flag. 
- When I/O transfer is started, the device status flag is unset (usually '0') to indicate that the device is busy doing a transfer. 
- When the tranfser is complete device status flag is updated (usually '1'); this means device is idle and ready to perform another I/O transfer. 

Protocols for programmed I/O transfer using device flags:
•**Busy Waiting**: if the device flag is 1 (idle) then reset it and transfer data, if it is 0 (busy) then repeat.
• **Polling**: if the device flag is 1 then reset it and transfer data, if it is 0 then perform another task for a fixed time, then repeat.

###### A generalized I/O program
In general terms we could synchronize the CPU and a device by carrying out the following kind of program (output. )
![[Generalised IO program.png| 200]]

**Busy Wait Strategy**
•load next data to send to I/O device x;
•  initiate I/O device x;
•  test I/O device x’s status flag;
•  if flag not set,
	•repeat last instruction (test).  /*wait*/
	
•  write data to device

**Polling Strategy**
•  load next data to send to I/O device x;
•  initiate I/O device x;
•  test I/O device x’s status flag;
•  if flag not set,
	•Do something else for a while, and go to previous step (test) 
•  write data to device

Disadvantages of Polling are:
	- Unresponsive $\to$ if device flage becomes idle just after being polled, then transfer must wait until next poll
	- Multiple Devices $\to$ Faster devices slowed down by slower devices
	- Complexity $\to$ Complex programming task. 
	
### Handling Input / Output

###### Interrupt-Drive I/O
- With programmed I/O processor has to wait for I/O module to be ready
- An alternative is to issue an I/O command and do some other useful work
- When ready I/O module will interrupt the processor
- The processor executes data transfer and resumes processing

![[Handling IO.png| 200]]


**Simplified mechanism for processing interrupt**
- When a device is ready for I/O transfer its status flag is raised and an interrupt request (IRQ) is sent to the CPU. 
- Processing and execution of the current instruction is completed and request is accepted by the CPU. Device sending the request is identified. 
- The address of the next instruction from the background process about to be executed, and the status flag is saved. 
- Contents of the PC are replaced with the next instruction. 
- Context is saved
- Execute the I/O
- Restore context
- The next instruction is taken (from before interrupt)

If while servicing a device another device interrupts then device priorities are assigned. Each I/O device is given a priority and when the device sends an interrupt request its priority is compared with the currently operating priority. 
An interrupt request will not be accepted unless the priority of the device issuing the interrupt request is higher than the operation priority of the current processes. 
Use of stack to save and restore contexts. 

>[!success] Advantages
>- Are typically less wasteful of CPU time 
>- Generally more responsive than polling
>- Good for controlling multiple devices

> [!failure] Disadvantages
> - Need special hardware to support a fast interrupt system
> - "Context switching" is costly in terms of CPU time; 

### DMA: Direct Memory Access
When large volumes of data are to be moved DMA is used as it is much more efficient. DMA allows access to memory independently of CPU. 

DMA works as such;
	- CPU starts the transfer
	- CPU can do something else
	- CPU is interrupted when transfer is completed

DMA is useful any time the CPU cannot keep up with the rate of data transfer, or where the CPU needs to perform useful work while waiting for a relatively slow I/O data transfer.

---