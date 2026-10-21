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
## OUTPUT
<img width="736" height="167" alt="image" src="https://github.com/user-attachments/assets/b840098b-4676-4960-a27e-dbdbdb20ce64" />



cat < file2
## OUTPUT
<img width="667" height="167" alt="image" src="https://github.com/user-attachments/assets/5ef64d77-25a2-497a-b475-f8995d87d5a7" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="587" height="68" alt="image" src="https://github.com/user-attachments/assets/2c7b2154-18d8-44fc-9fd1-0dcb1c4ec386" />
 
comm file1 file2
 ## OUTPUT
<img width="557" height="302" alt="image" src="https://github.com/user-attachments/assets/9e75f00f-a6b0-4a12-9dc5-eb92ca682f32" />

 
diff file1 file2
## OUTPUT
<img width="637" height="343" alt="image" src="https://github.com/user-attachments/assets/9ac62575-2453-4f5d-a8ab-b36c856976dd" />


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




cut -d "|" -f 1 file22
## OUTPUT
<img width="642" height="136" alt="image" src="https://github.com/user-attachments/assets/7f36d78a-84c9-4688-919a-6f3a9c50f180" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="603" height="137" alt="image" src="https://github.com/user-attachments/assets/42559aa3-6e6b-44f3-946f-1ddef02c1c7f" />


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
<img width="602" height="102" alt="image" src="https://github.com/user-attachments/assets/0929cfe8-da3a-47f2-9dbb-f5cbea5803e5" />



grep hello newfile 
## OUTPUT
<img width="557" height="75" alt="image" src="https://github.com/user-attachments/assets/eb736d4b-46e5-44cb-99db-95a927903188" />




grep -v hello newfile 
## OUTPUT
<img width="558" height="70" alt="image" src="https://github.com/user-attachments/assets/b7931f91-244a-47f7-8945-8663ae24aaec" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="712" height="103" alt="image" src="https://github.com/user-attachments/assets/585c1aa4-0d4e-460a-8c12-f4704eea8669" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="736" height="75" alt="image" src="https://github.com/user-attachments/assets/22266245-e830-4add-8061-d5a9843898ce" />




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="548" height="92" alt="image" src="https://github.com/user-attachments/assets/3610667b-2a8b-459b-8c1a-859a9a446b2f" />


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

<img width="612" height="92" alt="image" src="https://github.com/user-attachments/assets/dde0ffa1-d60e-4228-a5a4-f6c876b920cd" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="600" height="91" alt="image" src="https://github.com/user-attachments/assets/19a7f263-4b78-4a3c-a280-5759a886f46c" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="642" height="92" alt="image" src="https://github.com/user-attachments/assets/94ca021a-d414-413d-8ea8-af055f56a902" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="521" height="65" alt="image" src="https://github.com/user-attachments/assets/476f019e-1156-4fc1-b009-153ea475c752" />



egrep '(world$)' newfile 
## OUTPUT
<img width="542" height="125" alt="image" src="https://github.com/user-attachments/assets/07596bb1-72a7-4599-b413-dfa586d9ebd9" />



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="616" height="122" alt="image" src="https://github.com/user-attachments/assets/71bfe0fb-e359-4738-a945-706b4841291d" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="501" height="58" alt="image" src="https://github.com/user-attachments/assets/95e895bf-e853-4311-8d02-0f68d3c94614" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="587" height="90" alt="image" src="https://github.com/user-attachments/assets/051e0e1a-8b8b-4314-9da5-36de631a7b04" />


egrep 'Linux.*World' newfile 
## OUTPUT


egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 
<img width="561" height="120" alt="image" src="https://github.com/user-attachments/assets/85f04219-5df2-4629-b52d-30786868965a" />


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
<img width="490" height="67" alt="image" src="https://github.com/user-attachments/assets/3f983a7c-d7ee-46e8-a74e-48d4a5c2969c" />



sed -n -e '$p' file23
## OUTPUT
<img width="503" height="55" alt="image" src="https://github.com/user-attachments/assets/05bd42ab-ec1a-4562-b214-0bf7d45703f2" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="576" height="271" alt="image" src="https://github.com/user-attachments/assets/b72ca526-65b8-4f82-8492-b360a6668a58" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="611" height="273" alt="image" src="https://github.com/user-attachments/assets/d2ddf603-03ad-426a-abbe-32c3e4124f9b" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="611" height="263" alt="image" src="https://github.com/user-attachments/assets/34608f01-1f84-412a-85f3-594ba8c50795" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="606" height="182" alt="image" src="https://github.com/user-attachments/assets/8af6759b-0b33-4935-9f4a-7dc5eb021b43" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="570" height="122" alt="image" src="https://github.com/user-attachments/assets/de1d05d8-84db-457d-9a07-f601458eca13" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="660" height="92" alt="image" src="https://github.com/user-attachments/assets/231c80b1-748b-479c-b08f-d813a7850848" />



seq 10 
## OUTPUT
<img width="441" height="332" alt="image" src="https://github.com/user-attachments/assets/ccee1b23-e36b-440e-8dc5-20cf9e30cf8e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="540" height="120" alt="image" src="https://github.com/user-attachments/assets/57460df7-cae0-4c27-b2e2-90d2a9206de7" />



seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT
<img width="500" height="152" alt="image" src="https://github.com/user-attachments/assets/6b9623c5-b952-44ac-b6a7-e7796d8a0d01" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="511" height="127" alt="image" src="https://github.com/user-attachments/assets/5529a5e1-1df9-4902-864e-503c7e4dae74" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="545" height="122" alt="image" src="https://github.com/user-attachments/assets/e745cd24-7354-4753-bbc5-04cb17ee6daa" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="665" height="123" alt="image" src="https://github.com/user-attachments/assets/88d84292-d44c-4082-a19d-1f4adce897e9" />



sed -n '2,4{s/$/*/;p}' file23
<img width="618" height="126" alt="image" src="https://github.com/user-attachments/assets/36e2260d-d756-4cbb-8bcc-cb5e6619877b" />


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
<img width="535" height="187" alt="image" src="https://github.com/user-attachments/assets/a079339a-bd1f-4e64-92c0-c5d511bfbebf" />


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

<img width="527" height="182" alt="image" src="https://github.com/user-attachments/assets/4cee3503-ba24-4305-89a9-023b6be18a5d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="623" height="225" alt="image" src="https://github.com/user-attachments/assets/a69910e0-cac7-4abf-bfb4-b481d2a7934e" />

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
<img width="537" height="102" alt="image" src="https://github.com/user-attachments/assets/7ccb7c81-76ad-4580-ac93-32efa18d4c43" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="696" height="102" alt="image" src="https://github.com/user-attachments/assets/d88face8-2918-4758-8e60-0d3531508810" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="575" height="322" alt="image" src="https://github.com/user-attachments/assets/cba9696b-ad7d-44a7-9539-2fb8ea04034a" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="792" height="393" alt="image" src="https://github.com/user-attachments/assets/5f1e6029-7231-4f17-94bf-ff3437d961af" />


tar -xvf backup.tar
## OUTPUT
 <img width="592" height="322" alt="image" src="https://github.com/user-attachments/assets/fe315e92-9330-45bd-9fd3-3e0d367ada96" />

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
<img width="798" height="120" alt="image" src="https://github.com/user-attachments/assets/d0d75f19-1025-4f13-999b-98361d3d979b" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="502" height="97" alt="image" src="https://github.com/user-attachments/assets/bfb20816-56ee-435d-850a-81625af87fa5" />


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
<img width="901" height="710" alt="image" src="https://github.com/user-attachments/assets/311e0d8b-8578-4bd8-8e7e-681770340d9f" />

 
ls file1
## OUTPUT
<img width="480" height="77" alt="image" src="https://github.com/user-attachments/assets/24b7a042-49f7-42ef-8aa1-193bff56a86c" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="613" height="247" alt="image" src="https://github.com/user-attachments/assets/2a5b6386-00d1-4105-b1ad-e71a4f17ec77" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="483" height="122" alt="image" src="https://github.com/user-attachments/assets/a837dc55-0ac4-4cba-ab6d-7872e7be9459" />


 
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
<img width="570" height="250" alt="image" src="https://github.com/user-attachments/assets/1de94846-bd8a-4a7c-a069-95acbfa7de66" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="697" height="128" alt="image" src="https://github.com/user-attachments/assets/81caf327-1a69-4b8e-8a7d-dec4573fd3bb" />


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
<img width="700" height="25" alt="image" src="https://github.com/user-attachments/assets/7d6b27ca-24ba-4d21-bd1f-ac45b7966525" />

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
