# Pipelining
---
*Date :*  22-11-2023 
*Module :* #CM12002 
*Teacher*: #FabioNemetz 
*Resources :*

---
##### Contents: 
> [[# ]]
> [[# ]]
> [[# ]]
> 
--- 

Pipelining is a technique for implementing instruction-level parallelism within a single processor.
Another instruction can be begun before the previous one is finished.

Generally when we execute a sequence of instructions it goes as such:
F D F E S | F D F E S | $\to$ Fetch Decode Fetch Execute Store

However with modern processors instructions can overlap:
![[Pasted image 20221122113752.png | 300]]
So as we decode the first instruction, we can start fetching the second and so on. 

However there are some problems with this method. 
- Branching $\to$ When we branch next instruction is fetched from somewhere else entirely. This causes the pipeline to break and causes a temporary drop in speedup as we re-fill the pipeline. 

- Instruction Conflicts $\to$ Most times result of one execution cycle is necessary for the next fetch cycle to start. This can cause complications in data flow through the processor. 

- Load Delays $\to$ Fetching values is relatively slow. Sometimes pipeline stalls when one stage takes unexpectedly long. 

- Unequal stage times $\to$ For a pipeline to flow smoothly each stage must take(roughly) the same amount of time. Otherwise the pipeline moves at the rate of the slowest stage. 

### Superscalar architectures
> **Latency** is a measure of amount of time between the start of an action and it's completion
> **Throughput** is the total number of such actions in a given amount of time. 

With pipelining we can improve the throughput however the latency of the processor is constant. If we manage the instructions in such a way most / all of the compelte in the same amount of time. 
![[Pasted image 20221128112558.png]]

###### Advantages and Disadvantages of Pipelining
 | Advantages                                              | Disadvantages                                                                                |
 | ------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
 | Instruction throughput increases.                       | Designing pipelined processor is complex                                                     |
 | Pipelining increases the overall performance of the CPU | Instruction latency increases in pipelined processors                                        |
 | Faster ALU can be designed when pipelining is used      | Solving problems for branch instructions becomes very difficult as pipeline length increases |
 |                                                         |                                                                                              |
