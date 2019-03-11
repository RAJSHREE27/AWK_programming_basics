# AWK programming basics

#### AWK utility is a pettern scanning and processing language. It Searches one or more files to see if they contain lines that match specified patterns and then performs associated actions such as writing the line to the standard output or incrementing a counter each time it finds the match.  

###### AWK file extension : *.awk*
###### AWK uses regular expressions in sed style for pattern matching

###### SYNTAX

```awk
  awk option 'selection_criteria {action}' filename
```
*if no selection_criteria is used , the action applies to all the lines*

###### shows the contents of a file

```awk
 cat filename
```

###### to print all the data of file  - *it matches 'print' statement by default*

```awk
 awk '{print}' file_name
```

###### to print the lines which match a certain string say - *'produce'*

```awk
 awk '/produce/{print}' filename
```

*to show only the second field of ech line*
```awk
  awk '/produce/{print $2}' file_name
```
###### '$0' shows all the fields

###### just like batch file , create an .awk file say  "batch.awk" writing '/produce/{print $2}' and then the below command will give the same output as above

```awk
  awk -f batch.awk file_name
```

##### Variables and Expressions

###### Variables and expressions can be used with awk as used with many programming languages . Here, the expression consists of strings , numbers and variables combined with operators.
###### AWK does not have any datatypes, every expression is treated either as a string or a number. However, awk has an ability to make conversions whenever required.
###### To define a variable , one only needs to name it and assign a value. Case distinction in variable names are important.
###### Variables are implicitly initialised as 0.
###### AWK provides s=certain comparision operators like > , < , >= , <= , == , != , etc.

##### BEGIN and END sections
###### If there is a requirement of printing statements at the beginning and ending of the program. The syntax to it is :
```awk
  BEGIN{action}
  .....
  .....
  END{action}
```



