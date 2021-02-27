# Flight-Network-Project-using-5-Data-Structures

**Data Structures**:
•	Hash Map (by Linear Probing) (Maps airport IDs to an array index)
•	Graph (by Adjacency List) (Stores flight routes)
•	AVL Tree (Stores the airport details based on their IDs)
•	Queue
•	Stack
•	Linked List

**About the Project**
Our dataset contains flight details. It has starting airports and destination airports along with their distances. From this we created a directed graph. We stored all the details of those airports, their names, IATA codes and airport IDs in an AVL Tree based on their IDs as they were unique. The hash map acts as a link between the graph and the airport IDs as the vertices in our graph are just the indexes of the array but the airport IDs are random positive integers so we could not directly work with them (a lot of space would be wasted if we did). What the hash map does is that it maps the IDs to an array of size 3333 (number of unique airports). We used the linear probing approach so we could get a unique index in the array for every airport ID. This unique index is the index in which the graph stores the edges for that vertex. The graph array and the hash map array are two different arrays. 

**Functionality**
•	Search airport name and IATA code using the ID. (AVL Tree traversal)
•	Search flights from an airport. (Gets edges from the vertex, sends them to AVL Tree and prints the details after searching)
•	Shortest direct or indirect path between two airports. (Breadth first traversal using a parent and distance array)
•	Get distance and time of flight between two airports. (Search weight of edge between two vertices)
•	Print the whole database. (In order traversal of the AVL Tree)

**Test Inputs**
Print Airport details using ID: 2223 (For Islamabad)

Search flights for an airport: 2207 (For Lahore)

Shortest path between two airports:
	For direct : 2223 and 2207
	For Indirect: 2207 and 1

Distance between two airports: 2223 (Islamabad) and 2206 (Karachi)
