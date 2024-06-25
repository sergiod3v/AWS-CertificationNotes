## DR Planning
- Defined by _**SLA**_:
	- _**RTO (Recovery Time Objective)**_
		- Maximum time your app can be down
	- _**RPO (Recovery Point Objective)**_
		- Max time data can be lost in your app
			- Frequent Access might be minutes
			- Infrequent Access might be _**hours**_
		- Point of rollback
			- how much time has to be rewinded in case of failure
	- The RPO defines the point-in-time to which you wish to recover and the RTO defines the length of time required for recovery. The SLA is more general and the BCP is a Business Continuity Plan.

## Hyperconverged
- HCI (Hyperconverged Infrastructure)
	- Software defined storage
	- Virtualization
## File Integrity Monitoring (FIM)