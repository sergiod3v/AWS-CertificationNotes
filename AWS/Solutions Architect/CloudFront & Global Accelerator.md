- CDN using Edge Location (EL)
-  Customer -> Edge Location -> AWS -> Edge Location -> Customer
- req caches and is returned again instantly if needed
- serves as a "host" for a backend service, ALB & EC2 for example
- you can choose how many cloudfront endpoints ou want yo use
	- all 200
	- 100 least expensive
	- specific
- Invalidate Cache bypassing the TTL (time to live) 
	- in case backend changed
	- in case you want an already fetched file to update
### Global Accelerator - Anycast IP
- all edge locations use the same IP ( anycast )
- ush mucho sapo leyendo mis notas xddd
-  GA chooses closest server and connects you to it
- can be used by:
	1. Elastic IP
	2. EC2
	3. ALB
	4. NLB
	5. public or private