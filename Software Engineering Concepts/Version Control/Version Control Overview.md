# What is Version Control
Version control is a system that records the changes to a file or a set of files so that you can recall specific versions later.
## Types of Version control
### Local Version Control System
LVCSs have local databases that store all the changes to files under revision control. They work by keeping patch sets(the differences between files) in a special format on the disk;it can then re-create what any file looked like at any point in time by adding up all the patches.
### Centralize Version Control System
CVCSs have a single server that contains all the versioned files, and a number of clients that check out files from that central place.
#### Pros
- enables collaboration
- everyone knows what everyone else on the project is doing
- Administrators can control who does what
#### Cons
- single point of failure 
	- risk losing everything
### Distributed Version Control Systems
DVCSs have a server or servers that each client's computer communicates with. Each client computer also has a full mirror of the repository. Essentially, a remote repository or repositories communicates with and updates to many local repositories.
#### Pros
- enables collaboration
- everyone knows what everyone else on the project is doing
- easy to back up any failed remote repos
#### Cons
- concepts related to distributed systems such as merge conflicts have a high learning curve
# What is the most commonly used DVCS today?

 