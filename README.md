
      In a class, students have friendships. We represent friendships as a graph, where each student is a node
and a friendship is an edge. Write a Python program using Depth-First Search(DFS) to explore and print
all friends reachable from a given student.

Example Graph:
Graph = {
‘A’: [‘B’,’C’],
‘B’: [‘D’],
‘C’ : [‘E’],
‘D’ :[],
‘E’:[]
}

Task:
1. Implement DFS (using stack or recursion)
2. Start from student A
3. Print the order in which students are visited.

Expected Output:
A B C D E

Bonus:
Allow the user to input any student’s name and print all friends reachable from that student.

Submission:
Rename file as your ID_df_friends.py.
Make sure your code is properly commented.
