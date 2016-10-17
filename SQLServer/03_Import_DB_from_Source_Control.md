##Import Database from Source Control

---

<br><br>

### 1. Connect
Connect to the database you wish to import into

![Credentials](documents/assets/conn1.PNG)

The example screenshot shows a connection to an SQL Server Express instance on the network.


__Hint__:

Leave the Server field empty if the instance is on the same computer from where you are running gitSQL.

__Are you connecting to a full instance of SQL Server?__

Try leaving the instance  field empty and enter 'localhost' or the Computer IP/Name you wish to connect to.

A test button is available at the bottom right of the screen. This needs to be pressed before we can continue to the next stage.

Any connection issues will be shown in the console to help diagnose problems.
![Console](documents/assets/conn2.PNG)

<br><br>

### 2. Select

Select __Import New__ and then __Next__.
![ImportOption](documents/assets/importnew.PNG)

<br><br>

### 3 .gitSQL

Select the source control path you wish to import from.

![SCPath](documents/assets/gitsql1.PNG)

Press Run.

![ImportConfirmation](documents/assets/import-confirmation.PNG)

Select __Yes__ if you are happy to overwrite if the database already exists locally.
Select __No__ if you wish to export the latest database changes first.

<br>

![PopulatedWithProgress](documents/assets/import-progress.PNG)

gitSQL will then discover objects and data from the source control directory and populate an objects list and then process the list.

__N.B.__ You will be prompted if more than one database is found so you can select which database you wish to import.
