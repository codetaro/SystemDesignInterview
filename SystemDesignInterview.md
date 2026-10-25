# System Design Interview: An Insider’s Guide

## FORWARD

- [x] CHAPTER 1: SCALE FROM ZERO TO MILLIONS OF USERS

- [x] CHAPTER 2: BACK-OF-THE-ENVELOPE ESTIMATION

- [x] CHAPTER 3: A FRAMEWORK FOR SYSTEM DESIGN INTERVIEWS
  - Step 1 Understand the problem and establish design scope: 3 - 10 minutes
  - Step 2 Propose high-level design and get buy-in: 10 - 15 minutes
  - Step 3 Design deep dive: 10 - 25 minutes
  - Step 4 Wrap: 3 - 5 minutes

- [x] CHAPTER 4: DESIGN A RATE LIMITER
  - Token bucket
  - Leaking bucket
  - Fixed window counter
  - Sliding window log
  - Sliding window counter

- [x] CHAPTER 5: DESIGN CONSISTENT HASHING
  - Hash ring

- [x] CHAPTER 6: DESIGN A KEY-VALUE STORE
  - CAP theorem
    - **Consistency**: all clients see the same data at the same time no matter which node they connect to.
    - **Availability**: any client which requests data gets a response even if some of the nodes are down.
    - **Partition Tolerance**: the system continues to operate despite network partitions (a communication break between two nodes).
  - A **vector clock** is a [server, version] pair associated with a data item. It can be used to check if one version precedes, succeeds, or in conflict with others.
  - Quorum consensus
    - If R = 1 and W = N, the system is optimized for a fast read.
    - If W = 1 and R = N, the system is optimized for fast write.
    - If W + R > N, strong consistency is guaranteed (Usually N = 3, W = R = 2).
    - If W + R <= N, strong consistency is not guaranteed.

- [x] CHAPTER 7: DESIGN A UNIQUE ID GENERATOR IN DISTRIBUTED SYSTEMS
  - Multi-master replication
  - UUID (128-bit)
  - Ticket Server
  - Twitter snowflake approach
    - Sign bit: 1 bit
    - Timestamp: 41 bits
    - Datacenter ID: 5 bits
    - Machine ID: 5 bits
    - Sequence number: 12 bits (reset to 0 every millisecond)

- [ ] CHAPTER 8: DESIGN A URL SHORTENER

- [ ] CHAPTER 9: DESIGN A WEB CRAWLER

- [ ] CHAPTER 10: DESIGN A NOTIFICATION SYSTEM

- [ ] CHAPTER 11: DESIGN A NEWS FEED SYSTEM

- [ ] CHAPTER 12: DESIGN A CHAT SYSTEM

- [ ] CHAPTER 13: DESIGN A SEARCH AUTOCOMPLETE SYSTEM

- [ ] CHAPTER 14: DESIGN YOUTUBE

- [ ] CHAPTER 15: DESIGN GOOGLE DRIVE

- [ ] CHAPTER 16: THE LEARNING CONTINUES

## AFTERWORD