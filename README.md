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
<img width="487" height="490" alt="Screenshot 2026-10-25 124702" src="https://github.com/user-attachments/assets/6df8cf6b-578c-486f-8dda-c979287f53a5" />



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
<img width="503" height="216" alt="Screenshot 2026-10-25 125028" src="https://github.com/user-attachments/assets/63be1370-6673-4788-8c14-20a0d84ad7d9" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="610" height="237" alt="Screenshot 2026-10-25 125057" src="https://github.com/user-attachments/assets/04b3c7cc-8f0e-4cb0-8fc6-885e13cd2fe7" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="615" height="242" alt="Screenshot 2026-10-25 125136" src="https://github.com/user-attachments/assets/f0575061-bedd-4616-8332-746f236961c4" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
```
Hello world
hello world
```
 
grep Hello newfile 

## OUTPUT

<img width="547" height="145" alt="Screenshot 2026-10-25 125206" src="https://github.com/user-attachments/assets/79e774a5-35bb-4d7a-a77a-feea6eeacc38" />



grep hello newfile 
## OUTPUT

<img width="552" height="107" alt="Screenshot 2026-10-25 125235" src="https://github.com/user-attachments/assets/79105776-4313-4c64-bda9-3fb91aab86aa" />




grep -v hello newfile 
## OUTPUT

<img width="587" height="153" alt="Screenshot 2026-10-25 125308" src="https://github.com/user-attachments/assets/6ed1389c-0620-423d-a60c-72a8d6c2ca07" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="777" height="127" alt="Screenshot 2026-10-25 125406" src="https://github.com/user-attachments/assets/4c80557d-d96a-422f-a68e-5732ca12734d" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="736" height="75" alt="image" src="https://github.com/user-attachments/assets/22266245-e830-4add-8061-d5a9843898ce" />


grep -w -n world newfile   
## OUTPUT
<img width="627" height="165" alt="Screenshot 2026-10-25 125529" src="https://github.com/user-attachments/assets/5b5e5deb-cb34-409b-807b-5b76104108bc" />


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
<img width="721" height="152" alt="Screenshot 2026-10-25 125601" src="https://github.com/user-attachments/assets/e526e84e-9030-49cb-9ff0-d6223753ad4d" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="991" height="195" alt="Screenshot 2026-10-25 125717" src="https://github.com/user-attachments/assets/70f818c0-670b-4c9e-832b-9bec8efeddb6" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1095" height="202" alt="Screenshot 2026-10-25 125745" src="https://github.com/user-attachments/assets/2700e5d5-7057-48bd-9579-b451fdf097bb" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="936" height="167" alt="Screenshot 2026-10-25 125812" src="https://github.com/user-attachments/assets/fa9d7786-d8ca-49d8-ae93-1b14d43a4df1" />



egrep '(world$)' newfile 
## OUTPUT
<img width="871" height="193" alt="Screenshot 2026-10-25 125835" src="https://github.com/user-attachments/assets/a41dd057-858c-40af-a969-8abb0c2d3968" />



egrep '(World$)' newfile 
## OUTPUT
<img width="900" height="147" alt="Screenshot 2026-10-25 125856" src="https://github.com/user-attachments/assets/8e69b9cd-470b-45a0-b0f4-0a2076eb32fc" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="978" height="245" alt="Screenshot 2026-10-25 125933" src="https://github.com/user-attachments/assets/0550c7b5-d31d-40d9-abdd-8205f14ee871" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="808" height="146" alt="Screenshot 2026-10-25 125958" src="https://github.com/user-attachments/assets/40daacc8-5c4b-4a23-92f8-e8f80c5ceded" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="995" height="162" alt="Screenshot 2026-10-25 130022" src="https://github.com/user-attachments/assets/10d62e06-f177-4ac0-92cd-884523a66134" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="971" height="163" alt="Screenshot 2026-10-25 130043" src="https://github.com/user-attachments/assets/dc4c610a-3d4f-4bf0-a99d-097ecde7b70f" />


egrep l{2} newfile
## OUTPUT
<img width="780" height="202" alt="Screenshot 2026-10-25 130107" src="https://github.com/user-attachments/assets/a68879af-fbc2-46cb-a207-b6c3073a2c7c" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="867" height="265" alt="Screenshot 2026-10-25 130128" src="https://github.com/user-attachments/assets/9ce523bd-1799-4fa1-b3cf-4a97163b1dd2" />


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
<img width="448" height="131" alt="Screenshot 2026-10-25 130439" src="https://github.com/user-attachments/assets/743010fe-d538-46c8-a1a4-3d25bde04bb0" />



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


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="701" height="172" alt="Screenshot 2026-10-25 135225" src="https://github.com/user-attachments/assets/59501a80-6948-4261-87aa-ab0cd4d5c77d" />




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
bash: ./one: Permission denied


<img width="250" height="73" alt="Screenshot 2026-10-25 131403" src="https://github.com/user-attachments/assets/9402ad80-c973-4d2f-98f9-555a3033408d" />

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


## OUTPUT
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
<img width="650" height="117" alt="Screenshot 2026-10-25 131857" src="https://github.com/user-attachments/assets/d564e049-b8bd-4850-ab80-1bf2a1c2bc5a" />


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
<img width="858" height="178" alt="Screenshot 2026-10-25 132001" src="https://github.com/user-attachments/assets/8ccda8bf-c138-4320-8084-c6e3e3a3548d" />




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


## OUTPUT
<img width="842" height="265" alt="Screenshot 2026-10-25 132034" src="https://github.com/user-attachments/assets/04e45d22-36cc-440f-840f-b7833f5ac9fb" />



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
  
## OUTPUT

<img width="580" height="177" alt="Screenshot 2026-10-25 132107" src="https://github.com/user-attachments/assets/a110f922-cbd5-4af1-883b-39ca7675207b" />




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
<img width="600" height="243" alt="Screenshot 2026-10-25 132144" src="https://github.com/user-attachments/assets/85c2417c-8674-4d19-b65d-748cf10efe46" />



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
<img width="607" height="146" alt="Screenshot 2026-10-25 132219" src="https://github.com/user-attachments/assets/0ca24e2e-853a-4637-8552-f0c505048481" />



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
<img width="900" height="362" alt="Screenshot 2026-10-25 132256" src="https://github.com/user-attachments/assets/42958118-40a9-47b8-90f9-c7b7aea77358" />


 
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
## OUTPUT

<img width="545" height="437" alt="Screenshot 2026-10-25 132337" src="https://github.com/user-attachments/assets/9f74f724-1afc-4011-afc5-7d58aeb4993f" />

 
 
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
## OUTPUT

<img width="628" height="225" alt="Screenshot 2026-10-25 132407" src="https://github.com/user-attachments/assets/2ce33b94-943d-4799-94b9-a7309bf73514" />
 
 
 
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
## OUTPUT

<img width="435" height="233" alt="Screenshot 2026-10-25 132432" src="https://github.com/user-attachments/assets/36e2630d-6b9d-434a-b07c-79e609ec5d94" />
 
 
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
## OUTPUT

<img width="417" height="177" alt="Screenshot 2026-10-25 133007" src="https://github.com/user-attachments/assets/60c49e8d-bff4-4319-a439-4d0a1c1890c6" />

 
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
## OUTPUT

<img width="415" height="163" alt="Screenshot 2026-10-25 133051" src="https://github.com/user-attachments/assets/c783ecb7-d1d7-4a9a-96ce-73a94fc4c5de" />

 
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
## OUTPUT

<img width="453" height="237" alt="Screenshot 2026-10-25 133122" src="https://github.com/user-attachments/assets/ed63b178-65fc-4642-a668-ae33bf4fbbc0" />


 
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
<img width="427" height="232" alt="Screenshot 2026-10-25 133231" src="https://github.com/user-attachments/assets/7ce48127-f99d-4eb8-b5ed-45122227fbf0" />


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
<img width="332" height="77" alt="Screenshot 2026-10-25 133312" src="https://github.com/user-attachments/assets/c7362a10-5aec-437c-8c29-2d428be286aa" />


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
<img width="440" height="223" alt="Screenshot 2026-10-25 133352" src="https://github.com/user-attachments/assets/6e9e08df-2dfd-45ef-9564-e3496b43bebd" />



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
<img width="436" height="215" alt="Screenshot 2026-10-25 133436" src="https://github.com/user-attachments/assets/ca431235-9efd-4921-b1c4-a765f30814dc" />


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
<img width="485" height="372" alt="Screenshot 2026-10-25 133511" src="https://github.com/user-attachments/assets/e0429372-69c0-4903-a13b-e128ea753a1d" />

 
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

<img width="437" height="153" alt="Screenshot 2026-10-25 133617" src="https://github.com/user-attachments/assets/8254a9a3-63bf-4f87-a437-ba552826fb1e" />

 
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
<img width="456" height="192" alt="Screenshot 2026-10-25 133654" src="https://github.com/user-attachments/assets/874f6a4b-16ee-47ae-9592-eed39f5daf4a" />


 
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
<img width="737" height="208" alt="Screenshot 2026-10-25 133929" src="https://github.com/user-attachments/assets/f1fc5a49-619b-455e-90a9-90a351353903" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="803" height="175" alt="Screenshot 2026-10-25 134048" src="https://github.com/user-attachments/assets/d60c47d5-8805-47a1-ac2e-06401fcda5ad" />



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

<img width="580" height="140" alt="Screenshot 2026-10-25 134142" src="https://github.com/user-attachments/assets/f00e3497-2af0-4f10-9c2a-a963ba9e1fd5" />

 
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
<img width="665" height="241" alt="Screenshot 2026-10-25 134209" src="https://github.com/user-attachments/assets/a71be5cf-953e-414a-a442-54e3380097ff" />


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
<img width="690" height="242" alt="Screenshot 2026-10-25 134308" src="https://github.com/user-attachments/assets/8d7c75b7-cf29-459a-9371-f67428d2de99" />


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


<img width="450" height="392" alt="Screenshot 2026-10-25 134412" src="https://github.com/user-attachments/assets/e4760909-ba5c-4c1e-bb4e-229e5a2e9994" />
 
 
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
<img width="427" height="65" alt="Screenshot 2026-10-25 134444" src="https://github.com/user-attachments/assets/2c19cfc9-ebab-4893-8475-4bffa183d937" />


 
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
<img width="712" height="241" alt="Screenshot 2026-10-25 134509" src="https://github.com/user-attachments/assets/3cc381b8-7bdd-4aa5-866b-0f2c69244e28" />




# RESULT:
The Commands are executed successfully.
