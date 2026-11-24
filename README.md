# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
<img width="627" height="177" alt="image" src="https://github.com/user-attachments/assets/c3883557-408b-4457-bc6b-37839c655681" />

cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
<img width="650" height="198" alt="image" src="https://github.com/user-attachments/assets/f82768f9-86e0-4a1f-91ee-c5ba46e5365a" />

### Display the content of the files
cat < file1
## OUTPUT

<img width="571" height="81" alt="image" src="https://github.com/user-attachments/assets/fac420a0-542e-41d2-8803-4f282032caf3" />
<img width="576" height="197" alt="image" src="https://github.com/user-attachments/assets/4910b1c0-e52a-413f-b121-b3c44c09a613" />

<img width="663" height="315" alt="image" src="https://github.com/user-attachments/assets/860979dd-66aa-4c7f-aeb9-30c376d471ef" />

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
cut -c1-3 file11

## OUTPUT

<img width="617" height="123" alt="image" src="https://github.com/user-attachments/assets/60f21e7d-2112-4934-890d-5df043c00754" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="647" height="127" alt="image" src="https://github.com/user-attachments/assets/eb17ce44-5b0d-4949-9c13-230fb820d509" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="626" height="132" alt="image" src="https://github.com/user-attachments/assets/229b6fff-7ec0-48b3-993a-e2d94301c56c" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="568" height="77" alt="image" src="https://github.com/user-attachments/assets/ad611c81-a3c8-4acf-b3c4-c9557870f35e" />



grep hello newfile 
## OUTPUT


<img width="567" height="85" alt="image" src="https://github.com/user-attachments/assets/1add2bc5-ee14-4157-a5d3-ab7966645316" />


grep -v hello newfile 
## OUTPUT

<img width="567" height="85" alt="image" src="https://github.com/user-attachments/assets/78eadb31-0637-43fb-aa0e-76d582d18e0e" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="520" height="106" alt="image" src="https://github.com/user-attachments/assets/c6ded0a0-6162-44d6-9330-8d01a5d70db5" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="552" height="71" alt="image" src="https://github.com/user-attachments/assets/db2d4866-8899-42fa-bbbd-4c245bd80a8b" />


grep -R ubuntu /etc
## OUTPUT

<img width="571" height="83" alt="image" src="https://github.com/user-attachments/assets/ee88f7cd-e3ab-4c64-afdf-55bd03d6c64c" />


grep -w -n world newfile   
## OUTPUT

<img width="546" height="73" alt="image" src="https://github.com/user-attachments/assets/bcb37657-7eec-4796-b3e9-a5b20af502be" />

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="530" height="71" alt="image" src="https://github.com/user-attachments/assets/005aef58-5a62-4494-b9a1-f97b3f1887ac" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="550" height="93" alt="image" src="https://github.com/user-attachments/assets/0703d750-d76a-4483-87aa-94630d3c2a6a" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="1600" height="769" alt="image" src="https://github.com/user-attachments/assets/702c87f6-2f8b-4c87-b9e9-a759c001e7e7" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="587" height="122" alt="image" src="https://github.com/user-attachments/assets/ee42cec5-9956-4cbc-879b-262cfb7ebdee" />


egrep '(world$)' newfile 
## OUTPUT

<img width="587" height="122" alt="image" src="https://github.com/user-attachments/assets/a0554f5b-964b-406b-bdc3-6039b5a68b64" />


egrep '(World$)' newfile 
## OUTPUT
<img width="562" height="77" alt="image" src="https://github.com/user-attachments/assets/7700fc55-ea0e-4bc6-b998-388e12e4b7c5" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="800" height="601" alt="image" src="https://github.com/user-attachments/assets/5fdcd4c7-e861-4b88-8e9c-fcb7d23c84d0" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="533" height="98" alt="image" src="https://github.com/user-attachments/assets/436e1a1e-c854-469c-a66c-155c1f6cd445" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="571" height="81" alt="image" src="https://github.com/user-attachments/assets/b1c66fc9-a1cf-4ffc-acc6-845fd5c960ad" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="540" height="95" alt="image" src="https://github.com/user-attachments/assets/3b4d4554-c2cc-4f53-ade2-d1c9f6d4fcf9" />


egrep l{2} newfile
## OUTPUT
<img width="626" height="132" alt="image" src="https://github.com/user-attachments/assets/13f497a9-2415-4a5a-a099-32118bb804c4" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="561" height="105" alt="image" src="https://github.com/user-attachments/assets/4714694c-921a-4b83-b801-fa2b2e3ed1aa" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="613" height="126" alt="image" src="https://github.com/user-attachments/assets/6bee4cf7-89c9-4c68-ab49-4278f5affe37" />



sed -n -e '$p' file23
## OUTPUT

<img width="571" height="83" alt="image" src="https://github.com/user-attachments/assets/f4f6740b-cc2b-4475-82dc-6fc3c5e789fb" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="617" height="123" alt="image" src="https://github.com/user-attachments/assets/8f94ec65-6bdf-41ad-8aab-18b93b07b634" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="562" height="77" alt="image" src="https://github.com/user-attachments/assets/696c8aaa-d029-45b1-9e0f-621843992eb8" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="517" height="72" alt="image" src="https://github.com/user-attachments/assets/87e0a5ca-3aa0-4f4d-9621-9ca7d0c4af5c" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="550" height="93" alt="image" src="https://github.com/user-attachments/assets/fba4ad24-0d3d-4bc3-a352-1b64a15d73d4" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="520" height="106" alt="image" src="https://github.com/user-attachments/assets/80be6e9d-ad78-4f64-945f-73fcdb594d19" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="613" height="126" alt="image" src="https://github.com/user-attachments/assets/9a062a6a-c43b-4870-a3b4-50629ae7b068" />


seq 10 
## OUTPUT
<img width="568" height="77" alt="image" src="https://github.com/user-attachments/assets/67313778-919c-4dcf-9611-2cc5df0f9393" />


## OUTPUT

<img width="613" height="126" alt="image" src="https://github.com/user-attachments/assets/526c3514-791d-439e-8855-96c662c8ba34" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="568" height="77" alt="image" src="https://github.com/user-attachments/assets/0324b49e-d693-4b6e-8009-908b388f45ee" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="613" height="126" alt="image" src="https://github.com/user-attachments/assets/98c19825-9c2d-44b9-a942-6a3edbb9d263" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="587" height="122" alt="image" src="https://github.com/user-attachments/assets/7e1e62d1-d0da-48b4-ba3c-e7fd1774a7d4" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="552" height="71" alt="image" src="https://github.com/user-attachments/assets/b3cad8d4-9e80-4691-8f02-2c94e2736c40" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="520" height="106" alt="image" src="https://github.com/user-attachments/assets/51ba8ad6-69ca-421e-90bb-6c8bde33faee" />


sed -n '2,4{s/$/*/;p}' file23
## Output
<img width="520" height="106" alt="image" src="https://github.com/user-attachments/assets/2fdf5c6e-eec0-4103-9aa6-e266159abae5" />

#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

<img width="546" height="73" alt="image" src="https://github.com/user-attachments/assets/e202854d-b5f8-4c39-9af0-14210fbe94be" />

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT


 <img width="550" height="93" alt="image" src="https://github.com/user-attachments/assets/14130992-17a4-4e87-8cc2-a7ddf86c9407" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="626" height="132" alt="image" src="https://github.com/user-attachments/assets/9fbe0dcb-89f8-45d9-9eba-d8bf51c0b80e" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

## OUTPUT
 <img width="530" height="71" alt="image" src="https://github.com/user-attachments/assets/f5cb3818-cb37-4133-9922-dfa0d2f6c6b8" />

gunzip backup.tar.gz
## OUTPUT
<img width="550" height="93" alt="image" src="https://github.com/user-attachments/assets/2c090a4d-0d98-447d-86ab-863c1c17ff62" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="650" height="198" alt="image" src="https://github.com/user-attachments/assets/f067a708-2a05-4e01-b8dc-118e034cb6e6" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="566" height="88" alt="image" src="https://github.com/user-attachments/assets/f73a442e-c605-408c-b6a3-c8bc6c038134" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 <img width="517" height="72" alt="image" src="https://github.com/user-attachments/assets/8cb1b8c3-519d-41b6-b77e-eef45b3f76cb" />

ls file1
## OUTPUT
<img width="552" height="71" alt="image" src="https://github.com/user-attachments/assets/41814bc3-3bbe-403f-8f44-6c6576d9b894" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="571" height="72" alt="image" src="https://github.com/user-attachments/assets/a89f7d01-85fd-4e3d-a7e6-141bba48c061" />

abcd
 
echo $?
 ## OUTPUT

<img width="1600" height="769" alt="image" src="https://github.com/user-attachments/assets/1e9c5a8a-6b34-485a-892b-51aa0ec691a7" />

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```


# RESULT:
The Commands are executed successfully.
