    Joseph Lombardi
    COMP 271: Data Structures
    Lab 4
    Due 06/27/2018


####Question: What is the purpose of E in this class definition?

The E is a type parameter so in other words our Node class is a parameterized class.  The E allows us to create an instance of the Node class with any non-primitive type we decide to pass to it.  Though we are using the String type in this assignment we could create an instance of the Node class also using an Integer, Float, or any class type, interface type, or even another type variable.


####Question: What is the purpose of this in the second constructor definition?
The this keyword in the second constructor definition is calling the 2-argument constructor, passing in the data but always using null for the next member variable.   This is called an explicit constructor invocation.


####Question: What is the purpose of toString in this class definition?
The purpose of the toString() in this class definition is to show the hashcode for each node.  Every time we create a reference variable it calls toString() and displays the hashcode.  We can also compare the hashcode just for learning.  For example, if I enter the node name reference, joe in my case, it will show its hashcode.  If I enter hello.next it should show the same hashcode as the reference joe did.


####Question: Which way to create the list more clearly conveys the actual structure of the list?
Though I understand the structure of the list regardless how we create it, the clearest way to me was to create a reference to each node separately and then call node1.next = node2 etc...



####Question: What happens if you use the printNode method on this circular list?
You end up with a wonderful endless loop.

####Question: How would you describe the shape of any noncyclical structure you can build using the Node class? Furthermore, can you build structures with branches that look like trees, where a node can have more than one successor or neighbor?
I would describe the shape as linear because noncyclical means not being repeated.  A circular linked list would be the opposite of noncyclical.  A linkedlist is a sequence of elements where each element is linked to the next one and a doubly linkedlist is the same but has a reference to its previous element.  This structure does not look like a tree.  I would have to say no, you cannot build structures with branches that look lie trees, where a node can have more than one successor.

####Question: Would the same code work for an ArrayList?
Yes the same code works for both an ArrayList and LinkedList.  Both implement the List Interface.  I also tested the code to verify it works.

    jshell> final List<String> myArrayList = new ArrayList<>(Arrays.asList("hello", "joe", "what", "up"));
    |  Warning:
    |  Modifier 'final'  not permitted in top-level declarations, ignored
    |  final List<String> myArrayList = new ArrayList<>(Arrays.asList("hello", "joe", "what", "up"));
    |  ^---^
    myArrayList ==> [hello, joe, what, up]

    jshell> final Iterator i = myArrayList.iterator();
    |  Warning:
    |  Modifier 'final'  not permitted in top-level declarations, ignored
    |  final Iterator i = myArrayList.iterator();
    |  ^---^
    i ==> java.util.ArrayList$Itr@3ffc5af1

    jshell> while (i.hasNext()) {
    ...> System.out.println(i.next());
    ...> }
    hello
    joe
    what
    up

    jshell>