# reimagined-design-patterns

Give a summary description of Four design patterns that you choose from the following design patterns: **Adapter,  Builder, Composite, Decorator, Observer, Interpreter, State, Mediator, Memento, Prototype, Proxy**. In your summaries say:

- what kind of problem(s) you can solve with that pattern and when you use it, maybe with a short example
- how the pattern works, what the basic idea of the pattern is
- what the main advantage and what the the main disadvantage is of using this pattern
- Write a short summary for each of the four patterns, about half a page for each pattern (rather less than more). 

> Do not add diagrams, and do not try to give a complete description of the patterns as found in the books. Rather think of how you would explain the essential ideas of these patterns in a few sentences to a colleague while drinking coffee.

Proxy design pattern :

Example : Suppose in SW we(Host/client) have a 3rd party component. This component uses completely different type of function calls and arguments . This is not easily understandable to the client. So they have designed some sort of wrapper which is easily understandable and user friendly. This wrapper will have understandable callouts and objects. So client will call this with proper data I/O. Internally this wrapper will invoke the actual code and get the data for the host SW.

Advantage : 1. Host SW dont have to know about the internal complexity.
	    2. Host has to pass minimal no of parameter to the constructor.
            3. Less chance of error than direct Component calls.
	    4. Easily maintanable.
	    5. Security, if the actual code is Some security related module this method can hide it.

Disadvantage : 1. If the real code is accessed then it may cause problem as both SW compatibility may be less.


Observer design pattern : 

Example  : It is similar to Subsciribing to a perticular channel / Magazine . The publisher will be called subject and all the subscribers are called observer. So if any new things happens the observer will get to know from the Subject . This behavioural design pattern can be used if certain no of obejects are dependent on a single object. One to many connection.

Advantage : 1. Loose the coupling between objects.
            2. Subject only knows about the Subscriber interface.
	    3. No need to change subject every time new observer introduces. 
            
Disadvantage : 
            1. If there are some unknown observer then it can create problem. 


Builder design pattern :

Example : Suppose we want to create a complex object "phone" . It has various parameters to consider : "Size" , "OS" , "Battery Cap" etc. So there are n number of combination to be taken care if we pass in a single function argument . We have to remember all the argument types , order before calling the constructor. So instead of that if we decouple all the stuff , it would be easier to implement .  For example choosing a phone from some techwebsite . First chose OS , then choose Size , and all other combo before getting the final result . So this will help the SW developer not to remember the arguments , seqences . 

Advantage : 1. Code is readable. 
	    2. Minimized paramenter for constructor.
            3. less complexity.

Disadvantage : 1. Line of code increases.
               2. Each product will require seperate builder. 


Adapter design pattern  : 

Example: It is similar to the adapter available in the market , USB - ETH adapter , USB C to Lightning adapter. So the idea is if an Object interface is not compatible with each other , implementation of one Adapter object will solve the problem. It converts one interface to another form.

Advantage : 1. Makes code flexible. 
            2. Unlike proxy design it can be used to Swap the objects.

Disadvantage : 1. There might be long chain of adapters required if one is not sufficient . For examplt Type C - ETh (Type C - USB --> USB - ETH)
