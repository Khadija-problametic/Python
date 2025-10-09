#dfs traversal using stack
#the graph of the students friends with
#A is friends with B,C and Bis friends with D and C is friebd with E and D,E have no friends
g = {
    'A': ['B','C'],
    'B': ['D'],
    'C': ['E'],
    'D': [],
    'E': []
}
#making a dfs function to call friends Of the Students from graph
def dfs(g, i):
    v = set()  # to see the visited students
    sta = [i]  #stack to hold students as node from the graph

    while sta:
        s = sta.pop()
        if s not in v:
            print(s, end=' ')
            v.add(s)
            #add friend to stack it will check reversly
            for n in reversed(g[s]):
                if n not in v:
                    sta.append(n)
#printing friends of A
print('DFS traversal satrting from student A:')
dfs(g,'A')
print()
#printing friends of anyone from the graph 
#if there will no one with in the it will  than it will no go to the dfs
st=input("enter the name to satrt dfs: ")
print()
if st in g:
    print("the student list:")
    dfs(g,st)
else:
    print("student is not in the list")
      
