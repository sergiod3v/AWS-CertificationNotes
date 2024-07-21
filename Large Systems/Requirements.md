Architectural drivers.
### Types:
- Functional Requeriments / Features
	- What the system must do.
	- tied to the objective
	- describe system as black box
	- does not describe architecture
- Non-Functional requierements / Quality Atts
	- Techical quality attributes of the system
	- Architecture
- System Constraints
	- Time constraints - Strict deadlines
	- Financial Constraints - Limited budget
	- Staffing Constraints - devs avail
### Gathering Requirements
1. Identify all the actors in our system
2. Capture and describe all the possible use-cases/scenarios
3. User flow - expand each use case through flow of events
	1. Each event contains
		1. Action
		2. Data
- ### Example
	- "Allow people to join drivers on a route, who are willing to take passengers for a fee"
		- Actors: User & Driver
		- Use Cases:
			- Rider & Driver - Register
			- Rider & Driver login
			- Successful match
			- Unsuccessful match
		- (all events that can happen must be described)
- ### Use Cases - Deep dive
	- ### Sequence Diagram - Frequently Used
		- Example:
			- ![[Pasted image 20240705083328.png]]
		- Real Scenario *Data not represented yet:
			- User flow: 
				- Ride initialization:
					1. ![[Pasted image 20240705083524.png]]
				- Ride Completion![[Pasted image 20240705083857.png]]
		- Identify and briefly design a future API
			- Each interaction is an _**API call**_ between actor and system:
				- e.g: ![[Pasted image 20240705084011.png]]
			- Data flowing between those actors are arguments in that _**API call**_
	- ### Summary
		- Formal way to capture requirements:
			- Identifying,
				- actors
				- use cases 
					- Deep exapnd of the use case with interactions flow

- ## Quality Attributes
	- They have to be:
		- Measurable 
		- Testable
	- Ex: ![[Pasted image 20240710095234.png]]

- ## System Constraints
	- One of pillars for Software Architecture
	- Take no constraints lightly
	- Use loosely coupled architecture
	- types:
		- Technical Constraints
			- use certain technologies:
				- hardware/cloud vendor
				- programming language
				- database
				- platforms/browsers/OS, etc...
		- Business Constraints
			- Limited budget
			- Strict deadline
			- Architectural Patterns
			- Obligatory use of third-party services
		- Regulatory / Legal Constraints
			- Examples:
				- HIPPA (Health Insurance Portability and Accountability Act)
					- constraints on accessing patient's data
				- GDPR (General Data Protection Regulation)
					- limitations on colecting/storing/sharing user's data