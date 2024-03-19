A.	Identify a named self-adjusting algorithm (e.g., “Nearest Neighbor algorithm,” “Greedy algorithm”) that you used to create your program to deliver the packages.
a.	Nearest Neighbor Algorithm

B.  Write an overview of your program, in which you do the following:
1.  Explain the algorithm’s logic using pseudocode.
•	Read in the Packages CSV into the hash table.
•	Read in the distance CSV into an address dictionary and distances.
•	Schedule the packages on each truck depending on the delivery time, address, and special notes.
•	Find the nearest neighbor for the next package.
o	Check to see what the next delivery deadline is
o	Check if there are any similar addresses. 
•	Deliver the package to the address and repeat the process.
2.  Describe the programming environment you used to create the Python application.
	Pycharm
3.  Evaluate the space-time complexity of each major segment of the program, and the entire program, using big-O notation.
	Operation time for this program will depend on a few factors:
•	How many packages there are?
•	How is the Data formatted in the CSV?
If the data is sorted, and it’s a straight insert, then it’s a 0(n) however, I have some manipulation in this program, so it makes it 0(n log n) due to factoring the delivery deadline and the similar address. 
![image](https://github.com/ScriptGAL01/C950/assets/121732235/61ea69b9-06d6-46ae-959c-ced5e6f9706a)
4.  Explain the capability of your solution to scale and adapt to a growing number of packages.
	This program can take in an infinite number of packages through its CSV and hash table class. It can adapt with the delivery deadlines as well.
5.  Discuss why the software is efficient and easy to maintain.
	The software can record and report the trucks status and ensure that packages are being delivered as well as being delivered on time. Once the delivery starts, its as easy as sitting back and letting it run.
6.  Discuss the strengths and weaknesses of the self-adjusting data structures (e.g., the hash table).
•	Strengths
o	Fast Access to elements based on Keys (Hash table in data structures 2023)
o	Time complexity is O(1) (Hash table in data structures 2023)
o	Fast with big datasets (Hash table in data structures 2023)
•	Weaknesses
o	Many Collisions depending on how the hash table is designed (Hash table in data structures 2023)
o	Possible to unevenly distribute the keys (Hash table in data structures 2023)
C.  Write an original program to deliver all the packages, meeting all requirements, using the attached supporting documents “Salt Lake City Downtown Map,” “WGUPS Distance Table,” and the “WGUPS Package File.”
1.  Create an identifying comment within the first line of a file named “main.py” that includes your first name, last name, and student ID.
	See attached Code.
2.  Include comments in your code to explain the process and the flow of the program.
See attached Code.
D.  Identify a self-adjusting data structure, such as a hash table, that can be used with the algorithm identified in part A to store the package data.
	Hash Table
1.  Explain how your data structure accounts for the relationship between the data points you are storing.
The nearest neighbor algorithm works with the hash table class to retrieve packages from the hash table. Once it retrieves the package usually by the search method, it then can use the methods in the package class to retrieve the information that is with that package.

E.  Develop a hash table, without using any additional libraries or classes, that has an insertion function that takes the following components as input and inserts the components into the hash table:
•   package ID number
•   delivery address
•   delivery deadline
•   delivery city
•   delivery zip code
•   package weight
•   delivery status (e.g., delivered, en route)


F.  Develop a look-up function that takes the following components as input and returns the corresponding data elements:
•   package ID number
•   delivery address
•   delivery deadline
•   delivery city
•   delivery zip code
•   package weight
•   delivery status (i.e., “at the hub,” “en route,” or “delivered”), including the delivery time
I.  Justify the core algorithm you identified in part A and used in the solution by doing the following:
1.  Describe at least two strengths of the algorithm used in the solution.
•	It can handle multi – class programs.
•	No assumptions about the data beforehand!
2.  Verify that the algorithm used in the solution meets all requirements in the scenario.
3.  Identify two other named algorithms, different from the algorithm implemented in the solution, that would meet the requirements in the scenario.
	Dijkstras algorithm, Greedy’s algorithm
a.	Describe how each algorithm identified in part I3 is different from the algorithm used in the solution.
a.	Dijkstras algorithm 
i.	This algorithm could pick an unvisted vertex, or in this case package, and then calculate the distance to it and every package there after. In our case, Nearest Neighbor only looks at the next package and not all the packages. 
b.	Floyd-Warshall Algorithm
i.	This algorithm calculates the shortest distance between every single pair of nodes, then combines the shortest ones to get the final answer. Nearest Neighbor only looks at the next package distance and doesn’t take into consideration all the rest of the remaining packages. 

J.  Describe what you would do differently, other than the two algorithms identified in I3, if you did this project again.

	I think if I did this project again, I would start with trying to pair the packages together by similar addresses. I spent a lot of time trying to get the packages to arrive ontime but I did not notice until testing the requirements that many of the packages are going to similar addresses. I think this could lead to a decrease in miles per truck and less complexity.
K.  Justify the data structure you identified in part D by doing the following:
1.  Verify that the data structure used in the solution meets all requirements in the scenario.
a.  Explain how the time needed to complete the look-up function is affected by changes in the number of packages to be delivered.
	The time that it takes for the lookup function is important due to the number of packages that are inserted into the program. The more packages that need to be delivered, the more data the program must look through to get the correct package.
b.	Explain how the data structure space usage is affected by changes in the number of packages to be delivered.
The bigger the data structure is (the hash table in this case) the more time it will take to find the right packages and perform the delivery. This is like smaller the data structure is, the less work the program needs to do. 
c.	Describe how changes to the number of trucks or the number of cities would affect the look-up time and the space usage of the data structure.
If there are more trucks in the program, it’s possible that the program will need to call the search function more often to retrieve details for more than 1 truck at a time. If there was more than one city, the hash table would need to index the packages differently so that the retrieval of the data is faster. 
2.  Identify two other data structures that could meet the same requirements in the scenario.
a.  Describe how each data structure identified in part K2 is different from the data structure used in the solution.
•	Graph
o	A Graph is a data structure that has vertices and edges. In our program the vertices would be the packages and then the edges would be the distances. This is different than the hash table that uses an index to hold the package data.  
•	Binary Search Tree
o	A binary search Tree is made up of nodes or lists, and these are linked to other nodes. So, in our situation, the nodes would be the packages and then the other nodes would be linked to this. This is a little like what we did in the hash table, however the hash table had no recollection on all of the future nodes, just the one that would be coming next.
