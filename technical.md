# Technical Questions
> Questions about various technical topics
> It's not a complete list, I am looking forward to add more items and more topics.
> I will add some question with code later.
## Contents
 * [General Suggestions](#general-suggestions)
 * Software Development
	- [Exceptions](#exceptions)
	- [Inheritance](#inheritance)
	- [Frontend](#frontend)
	- [Reference/Pointer](#reference/pointer)
	- [Library usage and design](#library-usage-and-design)
 * Tools
	- [Git](#Git)
 * Networking
	- [TCP/IP Stack](#tcp/ip-stack)
 * Sysadmin
	- [General](#general)
## General Suggestions
 * It is good to ask not only how something can be done but in how many ways something can be done. Then you can ask which way is the best practice and if there is no best practice what are the trade-offs of various approaches.
 * It is a good idea to throw some bad code and ask the candidate to refactor it (preferably in a pair programming environment). Ask what should be done first and why. (ie. prioritize the changes.) Ask how long would each change the candidate suggests take and discuss how risky the change would be. Would any of the changes affect functionality in any way?
 * If you want to know if the candidate has hands-on experience on something, ask the names of related tools, commands, menu items etc. Names of things only someone who did that thing would know (and someone who only read about it online would not know). For example:
	- What command do you use to add a new rule to Linux firewall? Which parameter adds a rule and which one deletes a rule? (You don't need to ask the precise command with all the arguments.)
	- What tool do you prefer for 3-way merge resolution?
	- How do you live-migrate a VM to another host in the cluster in vSphere Client? (ie. where do you click?)
## Software Development
### Exceptions
 * (In whatever language and environment you are interviewing for) What happens (to the application) when some code running in a worker thread throws an unhandled exception?
### Inheritance
### Frontend
 * (For whatever UI framework you are interviewing for) What happens when you call a method which causes a new event to fire inside event handler code? (The answer may change depending on the framework.) (It is best if the candidate is given a sandbox environment for trial and error.)
 * How do you prevent the UI from freezing while waiting for a blocking operation to end. A regular example would be to write code which starts an HTTP request and shows a spinner in the UI until request is replied. Bonus; write code which handles exceptions in the thread and shows an error in the UI.
### Reference/Pointer
 * (For whichever language you are interviewing for) How can we check if two lists contain the same elements? (just assume these are integer lists for clarity.)
 * What is a copy constructor? When are they necessary?
 * (Java) What is a weak reference? What is WeakHashMap?
### Library usage and design
 * How to pass lists of objects between methods?
## Tools
### Git
 * How to undo a faulty merge commit? (For example we resolved some conflicts in a wrong way and we want to undo everything and run git merge again). What if we committed the faulty merge? The candidate can be given a repo in this situation and asked to rescue it with all the help from online git documentation and stackoverflow. What would be the best course of action to fix the repo if we pushed the commit too?
 * Candidate should be given a simple codebase with a few commits on a few branches and put into a situation which involves 3-way merge resolution. (For example merge a feature branch back to development branch which moved forward with other commits.) What should be done if the conflict cannot be resolved easily with mergetool and some parts of the code must be rewritten? What should we do if we want to use the whole file in one of the branches? (candidate should be able to find the command in stackoverflow event if he/she can't remember "git checkout --theirs / ours")
## Networking
### TCP/IP Stack
 * Can you trace a PC's network card's MAC address on the internet? For example can I find out the MAC address of someone who has connected to my server? (and call the authorities to arrest him using MAC address information for example?) (So basic yet so many people have weird ideas about MAC addresses.) Can you think of an example where MAC address information can be used to match a network connection to a host or user?
 * What does ping command do? Why is it so popular and useful? (Or why it's not as useful as people claim if you think otherwise?) (I think it's extremely useful btw :))
## SysAdmin
### General
 * Do you take backups of configuration files before modifying them? (Of course you can't ask this directly, just give a task and observe.)
 * How do you list users in a group in Linux? (groups) Can you write a line of piped commands which does the same / similar job? (in Linux users have default and additional groups so you need to use "id -Gn" command on all usernames and filter the usernames which are in the group you are searching)
