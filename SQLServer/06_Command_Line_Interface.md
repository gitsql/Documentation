## Command Line Interface (CLI)

---
<br><br>

> This feature is only available to licenced users

> A sample project is available on GitHub at https://github.com/gitsql/cli-gitsql-sqlserver

### Usage

```
gitSQL import/export -s <ServerName> -i <InstanceName> -a <WindowsAuth> [-u <Username>] [-p <Password>] -d <Directory> [-o <OptionsFile>] 

Argument list example:
         -s  :  localhost
         -d  :  "c:\temp\folder"
         [-a]:  false
         [-i]:  SQLEXPRESS
         [-u]:  sa
         [-p]:  sapassword
         [-o]:  "c:\temp\options.json"
```

### Usage Example

#### Export

```
gitsql export -s DESKTOP -i SQLEXPRESS -o opts.json -d "c:\source_control"
```

#### Import

```
gitsql import -s DESKTOP -i SQLEXPRESS -d "c:\source_control"
```

__Hint__:

-d is the path to the source control directory where the database has been exported to. An options file is required if more than one database is located in this directory.

### Options File

```
{
        "includeDrop": "false",
        "includeDependencies": "false",
        "includeIndexes" : "false",
        "includeConstraints": "false",
        "includeTriggers": "false",
        "replace":{
                "findMe": "SET QUOTED_IDENTIFIER ON",
                "replaceWith": ""
        },
        "db": "AdventureWorks2012"
}
```
