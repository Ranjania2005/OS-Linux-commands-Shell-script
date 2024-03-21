![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/f7e06ae0-d31c-4c77-875f-af51c6b99513)# OS-Linux-commands-Shell-scripting
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
cat < file2
## OUTPUT
![Screenshot (153)](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/79a6996a-fe57-4ab3-a2e3-73991550ee87)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot (154)](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/7a029b5b-1914-4679-a41e-357ba0e164bf)

comm file1 file2
 ## OUTPUT
![Screenshot (155)](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/19270f97-e9f3-491a-9319-f3463a16966a)

 
diff file1 file2
## OUTPUT
![Screenshot (156)](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/26a053ac-6871-49de-ad1b-45dcf44b9f85)


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
![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/631da9b9-b749-4a7f-8b9b-f893b7a46599)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/1d0339ad-db78-49fd-94dd-a4215c9f7a65)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/9301db1d-080f-499e-8254-7f8a94cc1c2f)


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
![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/a4556896-18e1-4b79-b0bf-4f92386a8b6c)



grep hello newfile 
## OUTPUT
![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/795092ff-57ca-426e-9163-05fe9f5df416)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/8d962ea5-1f9d-4686-8562-c588c61090f1)




cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/dd562c47-c033-4357-b28e-301159f061c7)



cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/c38c90a0-7eba-419d-8c77-b19111d2f609)




grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/a8822ae7-1abc-4f5a-a557-22fc10cda6f6)



grep -w -n world newfile   
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/982c7617-fe68-4f22-81df-3f277c6a1f3d)


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

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/8ff21abf-c23e-4fed-a6aa-b6e7d79c3512)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/62dadc41-98ce-492f-a9c3-e7a320c611b7)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/8a0926a3-f998-4ab9-97d9-97b6aef7941c)



egrep '(^hello)' newfile 
## OUTPUT


![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/67836b35-f8fe-4c6f-b6fb-b898b4f7914b)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/0cd62f9a-1c0a-4a97-ba24-7974e2ac2b89)




egrep '(World$)' newfile 
## OUTPUT
No output

egrep '((W|w)orld$)' newfile 
## OUTPUT


![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/3727ddd2-1426-4601-97f5-a63c479ff215)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/d743b5de-5f56-45d6-9ed8-4230e6b8a71e)



egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/f77f0d94-5e59-40b3-b242-976d11d44c06)


egrep 'Linux.*World' newfile 
## OUTPUT
No output

egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/5030e4f9-92f8-47a4-a2b1-5a2621183cb1)


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

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/9052bdea-d2fa-4e7d-9bb0-54139712f364)



sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/f1690dae-f2f9-4c84-a3bf-884fc4d5d94b)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/4b16bbd2-37d8-42e3-9eed-c10f11175357)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/2ba220de-ade4-4f4d-90ca-a00e29e48804)



sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/d707397b-13d7-4985-8d2a-e5cd05a061ea)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/fe8e413d-5e1f-41fc-a42a-dd3a4780fdb0)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/31d30966-7d1b-4c50-a6b1-08b37a0149a6)



seq 10 
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/c12972a4-8f0e-49ed-8ab3-853529b64e15)



seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/707704bc-e094-4c92-863a-9e2500f3f736)



seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/5ccaa641-44d9-40d3-a61d-0e63baa44478)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/fbb94a68-c786-4492-b59f-6e2205523f76)



seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/5f738216-7246-42ef-a5e4-8aec358c52b1)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/48e434d1-45d5-4ac6-b9a3-80b666e1c53d)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/84be6e77-0460-40ad-aa7f-f6cd177cd4f1)



sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/f92e6cf7-f668-4278-b756-cccef69a2043)


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

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/93b6fae1-26f8-4b2b-baf5-fcea1c54485b)


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
## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/fe3b156d-0ab9-4b9f-8eee-98c2763fed14)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/Ranjania2005/OS-Linux-commands-Shell-script/assets/151624950/e4426eff-6ac8-4ef9-a78e-540b94ce6aa0)

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
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
