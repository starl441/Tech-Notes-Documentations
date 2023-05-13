# Introduction

Bash scripting script usually have .sh extension by giving extension to the file while programming and after programming the code will be represented with colors to understand the script .Its a good practice to use shebang \[#!\] along with the file path of the bash at the start of the script.

  

Bash is in interpreted language just like python.We use # to comment .

  

**Let us create a hello world script :**

1.We will create a file with .sh extension

```bash
touch bashv1.sh
```

[2.you](http://2.you) can get the bash path using command which bash

```bash
which bash
```

  

2.We will open it using vim editor and start the script by typing shebang text in the file.

```bash
#!/usr/bin
```

  

3.We will use echo to the print the statements remember we can use this language in CLI as well.

```bash
#!/usr/bin
echo "Hello world"
```

  

4.We will save the file and exit.

[5.Now](http://5.Now) to run the script we use ./ command or bash command

```bash
./bashv1.sh
bash bashv1.sh
```

  

6.We will get an error "Permission denied" because we don't have read and write permisssions for the file to give the file permissions we use chmod.

```bash
chmod 777 bashv1.sh
```

  

[7.To](http://7.To) check if the file got the permission or not use command ls -al

```bash
ls -al
```

  

[8.Now](http://8.Now) run the script it will work.

```bash
./bashv1.sh
```

  

* * *

**Variables:**

  

There are two types of variables :

1.system variables

Eg: pwd,ls,cat \[Note:ls is a variable which saves the list of all directories in linux this logic applies to all commands\]

2.user defined variables

  

To call a system variable we use $

```bash
#!/user/bin
echo 'Hello world'
echo #PWD
```

  

  

To declare a user defined variable we can directly declare it and to call the variable use $

```bash
#!/user/bin
echo 'Hello world'
echo #PWD
x=10
echo $x
```

  

  

To do expressions like adding two numbers we need use tuples with $ ((expression))

```bash
#!/user/bin
echo 'Hello world'
echo #PWD
x=$((10+2))
echo $x
```

  

  

**NOTE:** we can use cat command to display the text inside the file. cat [bashv1.sh](http://bashv1.sh)

  

* * *

**User input:**

  

We use 'read' for the user input just like python 'input'

```bash
#!/user/bin
read age
echo $age
```

To enter the user input in the same line we use -p

```bash
#!/user/bin
read -p 'Enter your age: ' age
echo $age 
```

  

If you wanted to hide the input that the user is giving then we use -sp

```bash
#!/user/bin
read -sp 'Enter your age: ' age
echo $age 
```

  

To declare an array use -a

```bash
#!/user/bin
read -a just
echo "${just[1]}" #This prints the index 1 element of array just
  # double quotes are important don't use single quotes
```

  

To print the array without declaring any variable

```bash
#!/user/bin
read 
echo $reply
```

  

* * *

**Conditional Statements:**

  

**syntax:**

```bash
if [ condition ];
then
....
...
elif [ condition ]
..
[ statement ]
..
else
...
..
fi
```

  

**Note:**

1.we use fi at the end of the syntax to tell the it that its ended.

2.within list its important to leave spaces they are considered as indentations

  

To compare two numbers in bash we use the below instead of symbols:

```bash
-gt = greater than
-eq = equal to
-ne = not equal
-ge = greater than or equal to
-lt = less than
-le =less than or equal to
```

  

* * *

**Logical Operators:**

```bash
&& = and
|| = or
```

**Example:**

```bash
echo "Enter your age"
read age
if [ "$age" -ge 21] || [ "$age" -lt 35];
then 
echo "Since you re $age you can marry
else
echo "Lose Hope"
fi
```

  

* * *

**Loops:**

```bash
for loop
while loop
```

  

**For Loop Syntax:**

```bash
for i in range 1..10;do
..
.
..
done

for i in {1..10};
do
echo "$i"
done
```

**While Loop Syntax:**

```bash
while  [ condition ]
do
..
...
done
```

  

* * *