##How to source control between SQL Server and GIT

---
<br><br>

### Starting a new GIT repository with an existing Database

This is a scenario where you have a database, or a base database that you wish to use on your project.

Set up a new GIT repository or Clone an existing one which you wish to add the database to.

Run gitSQL and export all objects into your git folder.

HINT: Don't worry about folder names, try pointing to your root GIT repository directory - gitSQL will create a DB folder in there for you.

Here is an example of what to run once gitSQL has finished exporting the database.

```sh
  git add .
  git commit -m "Initial revision of database X"
  git push -u origin master
```

Alternatively - use a GIT client such as  [Source Tree](http://www.sourcetreeapp.com/ "Source Tree")

You now have a base SQL Server database committed to GIT.

### Make alterations in SQL Server

You are now ready to make changes to SQL Server as part of your development cycle.

Make a change to an object (or a set of objects) if it is applicable for the bug/issue/feature you are working on.

Run gitSQL and Export and select the relevant objects you wish to commit to source control.

Note: You do not need to export the entire database this time - just the objects which you have changed.

### Review your changes and then Commit

Run a GIT Diff or review the changes using a visual diff tool before commiting the changes.

Commit the changes once you are happy that the changes are OK to go into source control.


### Resuming/Collaborating later on

Multi developer environments will require database updates in order to keep up to date with the latest stream in GIT.


Use gitSQL to import either;

a) Individual objects which have changed since your last GIT PULL.
b) Entire database when you have not got the database installed locally. (Typically when you are resuming several months later, or you have a fresh development environment or you are coming into the project for the first time)

### Deploying a database to Live

gitSQL can be used to deploy directly from source control to a Live environment, but this should be done with caution as the static table data in source control may be different to what you require for the live environment.

There is the option to copy the entire database folder and then prefix the copied folder with __"Live\_"__.

gitSQL uses the folder name as the database name.

It is therefore possible to change the static data in the copied folder without effecting the development database.

Importing this new folder will then create an entirely separate live database.
