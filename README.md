# assignment2-tahatakgungor
assignment2-tahatakgungor created by GitHub Classroom

Banker’s Algorithm Project

Banker’s algorithm is a deadlock avoidance algorithm. It is run by the operating system whenever a process requests resources. It is named so because this algorithm is used in
banking systems to determine whether a loan can be granted or not. Whenever a new process is created, it must specify the maximum instances of each resource type that it needs, exactly.

Banker’s algorithm are characteristics:
• If any process requests for a resource, then it has to wait.

• This algorithm consists of advanced features for maximum resource allocation.

• There are limited resources in the system we have.

• In this algorithm, if any process gets all the needed resources, then it is that it should return the resources in a restricted period.

• Various resources are maintained in this algorithm that can fulfill the needs of at least one client.



Algorithm for checking to see if a state is safe:

1. Calculate the need matrix, and available resources A.

2. Look for row, R, whose unmet resource needs all ≤ A. If no such row exists, system will eventually deadlock since no process can run to completion

3. Assume process of row chosen requests all resources it needs and finishes. Mark process as terminated, add all its resources to the A vector.

4. Repeat steps 1 and 2 until either all processes marked terminated (initial state was safe) or no process left whose resource needs can be met (there is a deadlock).


Input:

4 // # of processes

5 // # of resources

//Max resource matrix

1 1 2 1 3

2 2 2 1 0

2 1 3 1 0

1 1 2 2 1

//resource allocation matrix

1 0 2 1 1

2 0 1 1 0

1 1 0 1 0

1 1 1 1 0

//resource available

0 0 2 1 2

----------------------------
Output:

Need Matrix :

0 1 0 0 2

0 2 1 0 0

1 0 3 0 0

0 0 1 1 1

Safe sequence is :

D A C B

Change in available resource matrix :

1 1 3 2 2

2 1 5 3 3

3 2 5 4 3

5 2 6 5 3

