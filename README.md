--------------------------------
**Author**
- Name&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Jaydeep Ingle</br>
- Email ID&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: jingle1@binghamton.edu</br>
- Project2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: GLobal Snapshots of a banking application</br>
- CS557&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Introduction to Distributed Systems</br>
- Dir&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: jingle1-project1</br>

--------------------------------------------------------------------------------------------
**Description:**
- BranchServer.java
This class makes use of BranchHandler class and starts serving the other
branches

- Branchhandler.java
It includes all the methods from the thrift generated interface
It makes use of threading to call sendMoney() method which will call the
transferMoney() method periodically.
It includes locking mechanism for locking various variables which are being
shared among the multiple threads

- BranchInfo.java
This is the template used for creating a list which will keep track of all the
branches

- Controller.java
This calls the iniBranch() method of Branchhandler.java
It also periodically calls the initSnapshot method to capture the snapshot among
the branches

- Channel.java
This class is being used for implementing channeling

- State.java
This class is being used for recording state of each class

--------------------------------------------------------------------------------------------
**Steps:**

```$make```</br>
- It will compile all the files including the above files plus the thrift generated files using the libraries.</br>

```$.branch.sh <branch-name> <port-number>```</br>
- This way we can start a branch on a specified port</br>

```$controller.sh <amount> <filename> ```</br>
- Makes use of amount to distibute evenly amon the branches. The branch info is being read from the filename</br>
--------------------------------------------------------------------------------------------

