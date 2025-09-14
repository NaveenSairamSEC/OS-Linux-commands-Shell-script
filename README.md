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

<img width="480" height="300" alt="Screenshot from 2025-09-14 15-51-53" src="https://github.com/user-attachments/assets/06778173-e063-4250-ab03-f57df6b9b70a" />


cat < file2
## OUTPUT
<img width="480" height="300" alt="Screenshot from 2025-09-14 15-53-34" src="https://github.com/user-attachments/assets/9ff01389-da89-4473-9f4d-b0aed751d29d" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="480" height="300" alt="Screenshot from 2025-09-14 15-54-28" src="https://github.com/user-attachments/assets/1a1e197f-2295-47ff-9d8d-787903331e60" />

comm file1 file2
 ## OUTPUT
<img width="480" height="300" alt="Screenshot from 2025-09-14 15-55-15" src="https://github.com/user-attachments/assets/09eeafbe-415b-4ebf-8f28-d7b27f8d82ad" />

 
diff file1 file2
## OUTPUT
<img width="480" height="300" alt="Screenshot from 2025-09-14 15-55-32" src="https://github.com/user-attachments/assets/bce09ab2-0ace-4974-8846-07e51d2f388b" />


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

<img width="480" height="300" alt="Screenshot from 2025-09-14 15-58-57" src="https://github.com/user-attachments/assets/4f8be9ce-3f97-4dce-986e-0396de7448c1" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="480" height="300" alt="Screenshot from 2025-09-14 15-59-10" src="https://github.com/user-attachments/assets/fc37d689-992e-4e05-9782-74f6ec0441fa" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="480" height="300" alt="Screenshot from 2025-09-14 15-59-45" src="https://github.com/user-attachments/assets/d15abfa8-f1b7-441a-9531-31a071d7d304" />


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

<img width="480" height="51" alt="Screenshot from 2025-09-14 16-04-27" src="https://github.com/user-attachments/assets/162e2d0e-5c1e-4e59-9963-e581fdb230e3" />


grep hello newfile 
## OUTPUT

<img width="480" height="51" alt="Screenshot from 2025-09-14 16-04-33" src="https://github.com/user-attachments/assets/33840d03-31e8-4e39-ba47-8064d3f71fdf" />



grep -v hello newfile 
## OUTPUT

<img width="480" height="51" alt="Screenshot from 2025-09-14 16-06-56" src="https://github.com/user-attachments/assets/155b198d-4a58-4f3a-b99f-7da16ae6d81f" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="485" height="68" alt="Screenshot from 2025-09-14 16-07-05" src="https://github.com/user-attachments/assets/36c312be-c363-4566-9204-ca563a4ec65c" />

cat newfile | grep -i -c "hello"
## OUTPUT


<img width="485" height="68" alt="Screenshot from 2025-09-14 16-07-05" src="https://github.com/user-attachments/assets/d4cbf337-0767-491f-85dc-44837966e102" />



grep -R ubuntu /etc
## OUTPUT


<img width="1310" height="1053" alt="Screenshot from 2025-09-14 16-08-53" src="https://github.com/user-attachments/assets/51b88dff-c64a-4153-8cba-6cb9721a4ce1" />


grep -w -n world newfile   
## OUTPUT

<img width="609" height="84" alt="Screenshot from 2025-09-14 16-09-45" src="https://github.com/user-attachments/assets/a9cda488-6247-4a5c-b979-fecee459947f" />


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


<img width="609" height="84" alt="Screenshot from 2025-09-14 16-12-23" src="https://github.com/user-attachments/assets/8e2b6f86-cc10-4e90-82a7-1379f7ca0dcb" />


egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="609" height="84" alt="Screenshot from 2025-09-14 16-12-29" src="https://github.com/user-attachments/assets/93ce0ee4-b1ed-4607-a847-b78872ffd5e0" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="609" height="84" alt="Screenshot from 2025-09-14 16-13-46" src="https://github.com/user-attachments/assets/542192bc-fc6b-49c5-bbe2-3c93c4ed4fe1" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="609" height="84" alt="Screenshot from 2025-09-14 16-14-07" src="https://github.com/user-attachments/assets/9e65abb7-529b-40ed-8851-ac40a4e2962e" />


egrep '(world$)' newfile 
## OUTPUT


<img width="609" height="84" alt="Screenshot from 2025-09-14 16-14-23" src="https://github.com/user-attachments/assets/9da2fea0-1229-43a9-aa7c-2c003591cc3e" />


egrep '(World$)' newfile 
## OUTPUT

<img width="609" height="84" alt="Screenshot from 2025-09-14 16-15-32" src="https://github.com/user-attachments/assets/f7ac752e-79bb-411c-9fb5-0c2eca40206a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="605" height="132" alt="Screenshot from 2025-09-14 16-15-53" src="https://github.com/user-attachments/assets/1be63485-8748-44e4-a461-7550db9f7d17" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="605" height="132" alt="Screenshot from 2025-09-14 16-16-14" src="https://github.com/user-attachments/assets/bf6ddfb6-2265-43da-b1b1-dd05702313e7" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="605" height="132" alt="Screenshot from 2025-09-14 16-16-36" src="https://github.com/user-attachments/assets/8cea3641-8029-465e-9ce2-50e681d5b5ad" />


egrep 'Linux.*World' newfile 
## OUTPUT


<img width="605" height="132" alt="Screenshot from 2025-09-14 16-16-36" src="https://github.com/user-attachments/assets/8c83fae8-49ec-4099-985a-b9c8ffd2a2ef" />

egrep l{2} newfile
## OUTPUT


<img width="605" height="132" alt="Screenshot from 2025-09-14 16-16-52" src="https://github.com/user-attachments/assets/732557c1-bf38-4c82-956f-c9e141af1620" />


egrep 's{1,2}' newfile
## OUTPUT 


<img width="605" height="132" alt="Screenshot from 2025-09-14 16-17-05" src="https://github.com/user-attachments/assets/0a80a5ee-5a67-43c0-81d2-1154482d45b8" />

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


<img width="605" height="132" alt="Screenshot from 2025-09-14 16-18-08" src="https://github.com/user-attachments/assets/62999400-b23e-45b7-a16f-0fb439ea43d6" />


sed -n -e '$p' file23
## OUTPUT


<img width="605" height="132" alt="Screenshot from 2025-09-14 16-18-20" src="https://github.com/user-attachments/assets/b3031959-0bbb-4c93-9412-32331fff94b3" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="615" height="192" alt="Screenshot from 2025-09-14 16-18-39" src="https://github.com/user-attachments/assets/1ab0c32f-ba7b-4377-8436-6da10b1e8ab1" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="615" height="192" alt="Screenshot from 2025-09-14 16-18-58" src="https://github.com/user-attachments/assets/c39b190d-eca9-43d6-9435-505247d0a881" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="615" height="192" alt="Screenshot from 2025-09-14 16-19-15" src="https://github.com/user-attachments/assets/6d8d156e-a331-41cf-94f0-574ef74a1f25" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="615" height="192" alt="Screenshot from 2025-09-14 16-19-27" src="https://github.com/user-attachments/assets/e310bd73-0fdd-4738-abcb-12274f53e779" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="615" height="103" alt="Screenshot from 2025-09-14 16-20-16" src="https://github.com/user-attachments/assets/cb3051f3-e62b-4cec-b4a3-86c675d9fa06" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="629" height="213" alt="Screenshot from 2025-09-14 16-20-34" src="https://github.com/user-attachments/assets/e6dcae97-1cb4-430a-bb5d-8a895756788b" />


seq 10 
## OUTPUT


<img width="629" height="116" alt="Screenshot from 2025-09-14 16-20-51" src="https://github.com/user-attachments/assets/4fb7a887-5d36-4885-8597-e0a4f2092fb5" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="629" height="116" alt="Screenshot from 2025-09-14 16-21-03" src="https://github.com/user-attachments/assets/2a3f2fb9-8a94-400f-b2be-008d311e0f6c" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="629" height="116" alt="Screenshot from 2025-09-14 16-21-17" src="https://github.com/user-attachments/assets/1f309047-71d0-4c20-9423-40a076c27114" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="629" height="116" alt="Screenshot from 2025-09-14 16-21-17" src="https://github.com/user-attachments/assets/8e02626d-3bd1-4f44-860b-642c704d0df9" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="629" height="116" alt="Screenshot from 2025-09-14 16-21-45" src="https://github.com/user-attachments/assets/8ebcbefe-85c8-46ff-9983-34941c6e7b9e" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="629" height="116" alt="Screenshot from 2025-09-14 16-24-41" src="https://github.com/user-attachments/assets/5ce92766-4e9a-4188-a073-d6d3326e7936" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="629" height="116" alt="Screenshot from 2025-09-14 16-24-54" src="https://github.com/user-attachments/assets/6368ab19-1674-4989-afc5-2bbaf34ef4eb" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="629" height="116" alt="Screenshot from 2025-09-14 16-25-16" src="https://github.com/user-attachments/assets/932feefd-231b-47d1-a52c-4efb08ce4bf2" />


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

<img width="629" height="116" alt="Screenshot from 2025-09-14 16-26-29" src="https://github.com/user-attachments/assets/464175b0-7aa7-4bab-853d-9883f0ac272e" />


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


<img width="471" height="127" alt="Screenshot from 2025-09-14 16-27-09" src="https://github.com/user-attachments/assets/8c5713bd-f582-47b8-8b54-883204fe33e7" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="524" height="196" alt="Screenshot from 2025-09-14 16-27-27" src="https://github.com/user-attachments/assets/7dd5170b-8e76-47a1-b2be-c75c9f1e6a03" />

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


<img width="524" height="196" alt="Screenshot from 2025-09-14 16-28-51" src="https://github.com/user-attachments/assets/cf9a24e9-fbea-4b64-b2fb-522e68b69ff6" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="524" height="196" alt="Screenshot from 2025-09-14 16-29-02" src="https://github.com/user-attachments/assets/5214954e-50c4-4465-a881-8ffd9406fad9" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


<img width="610" height="977" alt="Screenshot from 2025-09-14 16-34-40" src="https://github.com/user-attachments/assets/59003e96-2b77-405e-b1b4-6a7eb8a1d45e" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="975" height="994" alt="Screenshot from 2025-09-14 16-36-30" src="https://github.com/user-attachments/assets/932c811d-9bf1-4546-8ae3-aac8b3c333dc" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="859" height="69" alt="Screenshot from 2025-09-14 16-39-39" src="https://github.com/user-attachments/assets/54f33461-ac04-444c-916a-53ce5e13f342" />

gunzip backup.tar.gz
## OUTPUT

<img width="859" height="69" alt="Screenshot from 2025-09-14 16-39-43" src="https://github.com/user-attachments/assets/e191a067-c5db-4078-9f97-25c4b919d3f1" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="859" height="69" alt="Screenshot from 2025-09-14 16-40-51" src="https://github.com/user-attachments/assets/1d9877c8-e6d3-4a17-b22d-a55abcfccc4f" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="858" height="91" alt="Screenshot from 2025-09-14 16-42-31" src="https://github.com/user-attachments/assets/ba413069-b8a2-42ed-b875-97268952e571" />


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

<img width="786" height="282" alt="Screenshot from 2025-09-14 16-44-48" src="https://github.com/user-attachments/assets/c04304f7-f7f9-47e2-a319-5e0bde08e921" />

 
ls file1
## OUTPUT

<img width="478" height="70" alt="Screenshot from 2025-09-14 16-45-20" src="https://github.com/user-attachments/assets/4eea4f6b-ea59-4f1f-aa54-f8e2260c36dd" />

echo $?
## OUTPUT 

<img width="478" height="70" alt="Screenshot from 2025-09-14 16-45-31" src="https://github.com/user-attachments/assets/cbce1d67-6bbd-4dd4-b71b-038015ee3785" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="478" height="70" alt="Screenshot from 2025-09-14 16-46-33" src="https://github.com/user-attachments/assets/a0e11a22-fdf8-4b77-94a5-6b2409ff6ff5" />

abcd
 
echo $?
 ## OUTPUT

<img width="478" height="70" alt="Screenshot from 2025-09-14 16-46-33" src="https://github.com/user-attachments/assets/17388c5d-862a-494e-a794-d5618e40b7c8" />


 
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

<img width="479" height="187" alt="Screenshot from 2025-09-14 16-48-14" src="https://github.com/user-attachments/assets/aac5cd51-3a22-4408-9c64-cac4dae84399" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="589" height="147" alt="Screenshot from 2025-09-14 16-50-47" src="https://github.com/user-attachments/assets/82381508-00dc-48a5-a88e-845bb8a2dcae" />


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

<img width="589" height="147" alt="Screenshot from 2025-09-14 16-52-00" src="https://github.com/user-attachments/assets/fe5b015a-e41d-443a-bc8a-98ee0118e786" />

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

<img width="589" height="147" alt="Screenshot from 2025-09-14 16-52-45" src="https://github.com/user-attachments/assets/2fc48931-b9af-4215-8e3c-dcf82ea91345" />



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

<img width="531" height="330" alt="Screenshot from 2025-09-14 16-54-34" src="https://github.com/user-attachments/assets/565d5342-2992-465c-a89e-6e609a157520" />

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

<img width="574" height="119" alt="Screenshot from 2025-09-14 16-57-56" src="https://github.com/user-attachments/assets/d793d5f0-e706-4a15-9ebb-62cbf0ec6dc3" />

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

<img width="574" height="119" alt="Screenshot from 2025-09-14 17-03-17" src="https://github.com/user-attachments/assets/c649c5f1-f956-4198-a88e-ec2179bea226" />


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

<img width="574" height="119" alt="Screenshot from 2025-09-14 17-05-20" src="https://github.com/user-attachments/assets/932b135e-2b56-4e50-ad42-224ec60ce5dd" />

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

<img width="557" height="194" alt="Screenshot from 2025-09-14 17-28-15" src="https://github.com/user-attachments/assets/6bb7589c-7051-4ce6-8fbb-cbf485127991" />

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

<img width="876" height="183" alt="Screenshot from 2025-09-14 17-45-09" src="https://github.com/user-attachments/assets/fee63590-bc41-4d3d-bc12-2fcc551b83ee" />

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


<img width="520" height="183" alt="Screenshot from 2025-09-14 17-46-48" src="https://github.com/user-attachments/assets/b575978b-48f1-434c-9afa-aa8f488abd20" />

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

<img width="522" height="252" alt="Screenshot from 2025-09-14 17-48-25" src="https://github.com/user-attachments/assets/c5ded9e5-66f9-458a-b990-9f09c1feba95" />

 
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

<img width="652" height="166" alt="Screenshot from 2025-09-14 17-50-57" src="https://github.com/user-attachments/assets/36cc077e-752b-41f2-a584-2d97153f9ff9" />

 
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

 <img width="652" height="166" alt="Screenshot from 2025-09-14 17-51-46" src="https://github.com/user-attachments/assets/cb1d5b6b-69c2-4c4b-8fcc-30b1ff34ef6d" />

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
 <img width="652" height="166" alt="Screenshot from 2025-09-14 17-53-32" src="https://github.com/user-attachments/assets/ccc4ce33-c5e1-4638-923d-04e29a7a67bc" />

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

 <img width="652" height="166" alt="Screenshot from 2025-09-14 18-02-14" src="https://github.com/user-attachments/assets/c684695c-2475-4241-a13c-73bea4b66009" />

 ./funcex.sh 1 2
<img width="652" height="166" alt="Screenshot from 2025-09-14 18-03-44" src="https://github.com/user-attachments/assets/c9b98920-668c-4e70-8212-d868ba991d4c" />

 
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
<img width="388" height="338" alt="Screenshot from 2025-09-14 18-11-19" src="https://github.com/user-attachments/assets/6915065c-e9eb-4279-8c7d-67ca9bf1a8eb" />

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
 <img width="434" height="338" alt="Screenshot from 2025-09-14 18-12-07" src="https://github.com/user-attachments/assets/e2ceaa7a-dcd1-4136-a481-850ae1d2f67e" />

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
<img width="434" height="338" alt="Screenshot from 2025-09-14 18-13-18" src="https://github.com/user-attachments/assets/81c4b289-021b-4514-9193-bb518128cfba" />


# RESULT:
The Commands are executed successfully.
