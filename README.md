--------------------------------
**Author**
- Name&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Jaydeep Ingle</br>
- Email-ID&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: jingle1@binghamton.edu</br>
- Project2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: GLobal Snapshots of a banking application</br>
- CS557&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Introduction to Distributed Systems</br>
- Dir&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: jingle1-project1</br>

--------------------------------------------------------------------------------------------
**Description:**
- ```BranchServer.java```</br>
This class makes use of BranchHandler class and starts serving the other branches</br>

- ```Branchhandler.java```</br>
It includes all the methods from the thrift generated interface</br>
It makes use of threading to call sendMoney() method which will call the transferMoney() method periodically.</br>
It includes locking mechanism for locking various variables which are being shared among the multiple threads</br>

- ```BranchInfo.java```</br>
This is the template used for creating a list which will keep track of all the branches</br>

- ```Controller.java```</br>
This calls the iniBranch() method of Branchhandler.java</br>
It also periodically calls the initSnapshot method to capture the snapshot among the branches</br>

- ```Channel.java```</br>
This class is being used for implementing channeling</br>

- ```State.java```</br>
This class is being used for recording state of each class</br>

--------------------------------------------------------------------------------------------
**Steps:**

```$make```</br>
- It will compile all the files including the above files plus the thrift generated files using the libraries.</br>

```$./branch.sh <branch-name> <port-number>```</br>
- This way we can start a branch on a specified port</br>

```$./controller.sh <amount> <filename> ```</br>
- Makes use of amount to distibute evenly amon the branches. The branch info is being read from the filename</br>
--------------------------------------------------------------------------------------------

