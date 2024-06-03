
### ElastiCache
- same cache db manager
- Heavy changes from rds
- pre-fetch data so it can be cached and easily accessible
### ElastiCache - Solutions Architect
- Apps queries ElastiCache
- !queries -> queries from RDS
- cache hit -> exists in elasticache
- cache miss -> queries from rds -> stores in elasticache
- Only write the most frequently used data to the db

#### SA LEVEL
- ElastiCache supports IAM Auth for Redis
- IAM policies are only used for AWS API-level security
- Memcached -> SASL Cert

### Patterns
- Lazy Loading: all the read data is cached (stale data)
- Write Through: add/update data in cache when written to a DB