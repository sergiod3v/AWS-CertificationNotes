- ## Hyperthreading
	- Make a CPU look like 2 (1 virtual 1 physical)
		- Multithread
		- Paralellization of computations (multiple at once)
	- VT-x
		- Virtualization technology in the CPU
- ## Overcommitment
	- Utilize real resources for virtual machines well
		- Scenario
			- 2 CPUs
			- Each is quead core (x4 = 8)
			- Each is hyperthreaded (x2 = 16)
			- Total of _**16**_ Virtual CPUs
			- Run 4 VMs, each with 8 CPUs
			- 2:1 Overcommitment ratio
				- 2 virtual processors for each of the CPUs
- ## Memory Ballooning / Bursting
	- Feature of virtualization platforms
		- Unused, allocated memory for one guest can be used by another
- ## Memory Levels (Binary base 2 notation)
	- Base 2 numeric system for modern size notation  
	- ![[Pasted image 20240619082858.png]]
- ## Dedicated Host
	- Individual physical PC than its then virtualized and used only by you
	- Virtual Server:
		- demand the full virtual server available 