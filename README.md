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
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1

<img width="353" alt="os ex01 a" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/78ec2907-507e-4ba0-87f9-7cd1b286f513">

cat < file2

<img width="428" alt="os ex01b" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/f12feb40-b0b8-4188-abad-5dd2b620d859">


# Comparing Files
cmp file1 file2
## OUTPUT
 
<img width="421" alt="os ex01 c" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/6f0f9b44-af73-4524-897c-eefa150e84a3">

 ## OUTPUT
<img width="393" alt="os ex01 d" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/f4a34ec7-dfd9-4356-9134-0b6e3a8bd6e6">


## OUTPUT

<img width="395" alt="os ex01 e" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/0538025e-4907-43bc-9924-ab0d3742d0c2">



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


<img width="360" alt="os ex01 f" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/0c22bb0d-f504-4172-bcf8-dace27df9df6">



cut -d "|" -f 1 file22

<img width="347" alt="os ex01 g" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/231fcdd5-af11-4299-9921-3d8ab799b739">


cut -d "|" -f 2 file22

<img width="353" alt="osex01 h" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/fcd412ea-10e3-46b6-835f-4b5e2287e0af">


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

<img width="364" alt="os ex01 i" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/933366c8-1671-4c1c-8170-b52a94d018b8">



grep hello newfile 


<img width="359" alt="os ex01 j" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/3fed1b11-e694-4019-8a25-83b8d2f77205">



grep -v hello newfile 

<img width="363" alt="os ex01 k" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/1b5ef44b-ad67-4bc5-8af7-740b66be541d">



cat newfile | grep -i "hello"


<img width="363" alt="os ex01 l" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/e996db84-5716-4570-9067-44606fbeade8">


cat newfile | grep -i -c "hello"


<img width="364" alt="os ex01 m" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/c95cd02a-f93f-419e-b801-68a6ce35e063">



grep -R ubuntu /etc


<img width="362" alt="os ex01 o" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/dc0be921-c7ca-4227-9e25-37f090f8db2f">



grep -w -n world newfile   


<img width="356" alt="os ex01 n" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/aa01d676-7a1b-4bd1-94bb-40c85b1f8183">


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

<img width="352" alt="os ex01 p" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/28dcffd3-8561-44f5-b84c-fefcb9cb2d0f">


egrep -w '(H|h)ello' newfile 


<img width="356" alt="os ex01 q" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/2826ea53-bf3f-4fab-910f-9a512edff9d4">


egrep -w '(H|h)ell[a-z]' newfile 

<img width="347" alt="os ex01 r" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/d7c613b8-4ce1-443e-850c-096830d435d7">



egrep '(^hello)' newfile 


<img width="356" alt="os ex01s" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/7e0e766c-9d53-465b-b0eb-a1083037d465">

egrep '(world$)' newfile 

<img width="362" alt="os ex01t" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/6e0f2997-e44a-4e46-8cfe-4160d01d1585">


egrep '(World$)' newfile 

<img width="357" alt="osex1" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/37279e04-f6c6-4e6a-b8b9-2ee228bc6dd8">


egrep '((W|w)orld$)' newfile 

<img width="356" alt="os ex1 1" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/f66e26f6-3714-4928-912f-fc439a6f2b18">



egrep '[1-9]' newfile 
## OUTPUT



egrep 'Linux.*world' newfile 


egrep 'Linux.*World' newfile 

<img width="356" alt="os ex01 3" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/c5881d5e-b740-4d40-a4fc-07a3688e0d50">


egrep l{2} newfile


egrep 's{1,2}' newfile

<img width="357" alt="osex1 5" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/095f464d-2d2e-4644-8d04-8170da4b9329">


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

<img width="356" alt="ex01 6" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/dd1a2a99-7cf9-454c-96ff-41538edef4d9">


sed -n -e '$p' file23

<img width="366" alt="ex01 7" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/49d767f9-ff7a-4bdb-8bdb-8f3afa305f0c">



sed  -e 's/Ram/Sita/' file23

<img width="370" alt="ex01 8" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/c33bbfef-3acb-4383-8c7a-3131245d6211">



sed  -e '2s/Ram/Sita/' file23

<img width="358" alt="ex1 9" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/c6c0670b-2967-4d15-91fa-1f7345ed5cbd">



sed  '/tom/s/5000/6000/' file23

<img width="375" alt="ex1 10" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/99806077-f0c0-4087-8d36-d42d243fb746">



sed -n -e '1,5p' file23

<img width="374" alt="ex 1 11" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/dbdaff81-ec81-4c9d-80d5-66a229d217b3">



sed -n -e '2,/Joe/p' file23


<img width="371" alt="ex01 12" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/f349a64a-ac7b-47fd-9146-b38700a82bc9">


sed -n -e '/tom/,/Joe/p' file23

<img width="346" alt="ex 1 13" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/666b4acf-93aa-4735-a84e-0e41d24d2f01">


seq 10 

<img width="361" alt="ex 01 14" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/4dfeb057-9a4d-4499-86d5-f8a98415d8e7">



seq 10 | sed -n '4,6p'
<img width="368" alt="ex01 15" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/19114e0d-d180-454c-a14d-81c53e7f5bc8">



seq 10 | sed -n '2,~4p'


<img width="362" alt="ex01 16" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/21110bfb-9908-4c86-83ac-9c64c0dd7e1a">


seq 3 | sed '2a hello'

<img width="355" alt="ex 1 17" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/b32599a7-7d52-41cf-bec8-b071e4d0bc75">



seq 2 | sed '2i hello'

<img width="362" alt="ex01 18" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/5432d10f-af21-4ce9-bce1-d6ad2280756c">


seq 10 | sed '2,9c hello'


<img width="354" alt="ex01 19" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/cb7c0f14-74db-456b-9935-b08eb0db8af7">

sed -n '2,4{s/^/$/;p}' file23

<img width="365" alt="ex01 20" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/007efeae-a979-47ba-be4f-e46f6eb68d73">


sed -n '2,4{s/$/*/;p}' file23


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


<img width="368" alt="ex01 21" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/5020ae09-eb16-45c3-b920-2c1a897f4bce">

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22


<img width="351" alt="ex01 22" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/2bef2bcd-7115-43da-b304-e760789f6705">


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 <img width="367" alt="ex01 23" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/2c3cab0f-0346-4791-b41c-dfdf898472fd">

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
 

<img width="362" alt="ex01 24" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/59536983-8836-4415-8099-a3552472c33a">

 
cat urllist.txt | tr -d ' ' | tr -s '.'

<img width="331" alt="ex01 25" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/5ed3791c-04b2-40ac-8928-569bff72fd17">


#Backup commands
tar -cvf backup.tar *
<img width="364" alt="ex1 26" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/01c0979b-543b-4e59-8056-2cfbc773abc7">

<img width="359" alt="ex0127" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/5534a10a-e35d-4ed2-a711-2ed7974883ec">

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar

<img width="295" alt="ex01 28" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/5879605f-25f9-4f6e-8449-dcadd3c00d58">


tar -xvf back
<img width="368" alt="ex01 29" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/dcb32f81-6942-488b-b7a7-8322d67bef77">


gzip backup.tar
<img width="190" alt="3" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/b15a6e48-3c2c-48c4-881e-f8c07ada3f96">

ls .gz

 <img width="413" alt="1" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/2a5d0f0e-19cb-4469-9fe8-c1d7b24d626d">

gunzip backup.tar.gz

<img width="232" alt="2" src="https://github.com/Mythili7339267708/OS-Linux-commands-Shell-script/assets/144260246/92f7aee5-bc55-424b-a001-2d221da23d9d">

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
 
./strcomp.sh 
## OUTPUT


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
## OUTPUT 


# RESULT:
The Commands are executed successfully.
