##Export Database to Source Control

---
<br><br>

### 1. Connect
Connect to the database you wish to export from

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
Select the database you wish to export.

![DBList](documents/assets/select1.PNG)


![Objects](documents/assets/select2.PNG)

You will now have options to select all objects and data, None, Schema Only or Data Only.

Alternatively you may select items individually through the treeview control.

__N.B.__ The screenshot shows the free version which only loads four objects. The Unlimited version offers all objects for inclusion.

<br><br>

### 3. gitSQL

Select the source control path you wish to export to.

![SCPath](documents/assets/gitsql1.PNG)

Select Export.

![Direction](documents/assets/gitsql2.PNG)

Review the objects that you wish to export. Press back if you wish to make amendments - otherwise press Run.

![Progress](documents/assets/gitsql4.PNG)

<br>

You will now see a progress bar and completed items in the object list in the colour green once they have been completed.


![OutputExample](documents/assets/outputexample.PNG)

gitSQL will create a DB folder, and then a folder inside that which is the database name.

All exported objects will be in their type folders respectively as __.SQL__ files.

<br>


![DataFIles](documents/assets/datafiles.PNG)

The __DATA__ will be exported to the Tables\Data folder.

__Thats it!__

 You are now free to use a source control client or command line to commit your files into source control.
