# Ex01:OS-Linux-commands-Shell-scripting
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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/b6ad870c-004f-4c0a-b54c-df8d1912d0fc)


cat < file2
## OUTPUT
![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/a46042c8-c54b-42f1-9b4a-74baf2eb0d07)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/d6b15fdb-1d4f-4897-bd8d-b17f81be0d58)

comm file1 file2
 ## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/ad7b41ed-05b3-4c0f-b0ba-ce34ae65780b)
 
diff file1 file2
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/decbd51a-d226-4bb3-9c47-84e1f87ea32c)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/11703218-f76e-411f-bd03-4b9591eaf263)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/ebb106b7-42e1-4d83-aa5e-3db4c6890613)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/2d4d7ab1-e7d3-44e3-bfa3-22ae9fa9b2c2)


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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/7574b509-af47-495d-a936-3324e12385e6)


grep hello newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/dd14ed44-a8b4-46ea-a58a-ebe469398f54)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/d0b34937-61da-496f-b49a-066e0eabee24)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/5fe7b0cf-93b4-48af-9b3c-745fd1ce759b)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/50e8d222-2145-4157-94b1-2612033bfb6f)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/26289a57-23c4-479a-90a3-5987b8083f72)
![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/c1e08111-1963-47b4-8dbe-242fb53dbe24)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/b88ffd22-215e-437e-9237-f0229c00000c)


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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/4645bc9f-7cb7-4f4c-b613-95026ed79bda)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/2ae5a99b-8fc2-4f73-bd29-6c7841c91505)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/61b1a490-b00d-4765-8e63-0f7cfc343a38)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/cd674aec-5693-4c94-9813-f088f14bf7b9)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/db51a048-9d15-4468-bade-3d9a4ff5a32c)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/7f2a32b7-f1d9-4c64-b759-9f25f87678d0)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/11f94f31-6a9d-46fa-904b-66d396648b29)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/78395689-d3f9-41f5-a0e9-202b2e5c90ff)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/9ac794dd-6ddc-4568-af90-91d4e00b16fc)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/57e3ec00-1448-4722-82e2-dc7fa45c7875)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/1b470048-5189-4458-84d0-2f3a56c1e44a)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/81c815f4-b6ad-4cd2-8dd0-28e1e98ea43c)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/5aa872f9-452c-4cd1-9d97-d911060bcf6f)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/c72c743e-c087-45a2-ac03-afd6cd4c22de)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/307ea6f9-6cdf-4804-ad87-d4d0eccdef77)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/48dff1a7-e441-4eea-947b-59c286289c3f)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/ec47755d-74c6-41ba-982f-e5312edc20d0)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/27fbe205-4c75-4435-8856-2c1e69496c3b)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/da8239cc-315d-4733-a2af-7a542cd0bb32)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/a3f858f3-6fad-4a65-ba9a-68e84ea1ee15)


seq 10 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/94e48155-b88e-4950-a25c-319e488fe114)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/3f727e0c-fcd1-4578-ae2e-05e8d3dde2ac)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/7d184995-8bf8-4797-8234-0d34011199ee)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/c84e54ba-2d44-4c4b-8a2c-7f35551059ff)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/2a3d44f5-f703-4740-ae5d-830f162b8815)

seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/baee5b64-520d-4c5b-8bc9-577b98fdbecf)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/89aa4338-834d-46e7-ac78-efb35d8cf2e1)


sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/d014449a-9108-4f2f-af8b-54a9a8ec78d8)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/2908b277-dfc0-434a-940a-bc3393148e04)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/c804ac68-581d-4190-a8b4-9275d7272e4e)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/ac18f849-7ff2-44bb-8e75-7133e379d390)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/c38bb5f4-4889-4c9a-a432-296c73dbb87d)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/edaa0803-32b2-4b99-a1f0-9136b6ec9a80)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/7e54830c-fbc8-4469-92c2-023ed9c30ef4)
![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/fac60af6-4ab0-4106-a9a4-14642fbb8ce2)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/cf503fa9-fcc8-4941-bcdf-278ba35b106e)

tar -xvf backup.tar
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/43a968b4-c13f-4c4f-901e-30ed80916d47)

gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/12acd9fe-7a1a-4608-b236-f9c3dc4408d8)
 
gunzip backup.tar.gz
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/e2a72aa7-499a-4f4a-b75c-f91e1b5c7960)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/79e975ba-5784-4262-a73c-ad23eaafe0f1)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/693e3d5f-ca63-4a50-bc59-567eaee60c40)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/044b027e-a373-48af-8944-06907e1a901e)
 
ls file1
## OUTPUT
![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/00773732-bfb9-484f-a7ea-0863aab74720)

echo $?
## OUTPUT 

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/81b3248e-f50c-48ce-8aab-26ce6cd733d2)

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
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/c38027ae-c20e-49ad-8c72-a1f4c07cb28a)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/eb6a6997-1280-4052-ba0a-a7ff4159d4ce)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/73bd20f4-82ec-42bb-8d72-600775b86ac7)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/03a46092-4276-47f1-90d5-91cb37a43743)


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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/f695b995-a0d8-488d-8cdc-5bfa66dabd67)


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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/8156b872-566e-4799-bb69-3565a9f59915)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/5a134680-c7a9-42d5-ae1d-33658fcdae6e)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/64990b4e-71ad-4df5-bff6-e575bf7a701f)

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

 ![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/6f3eff84-913a-424c-a33a-12c9579791e4)

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
 
![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/2c12dc54-6664-4e50-99e5-878bea750652)
 
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
 
![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/c464479f-175b-40a7-a938-48a760405ff8)
 
 
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
 
 ![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/82702ac2-a474-451b-a0d8-ae80d6ee1b0e)

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
 
 ![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/0ee1f436-7f73-461f-87a2-45c5ff1ad396)

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

 ![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/7a20eecd-c11a-4587-a9ae-bb81fbb36307)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/100c24d8-7279-4728-b955-db0766f8a492)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/51ead935-5c0b-49c0-8196-5a7fdfe3e4e2)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/0e3fad38-c77c-4825-8291-5ad63692b1cc)

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

 ![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/4115d491-b8c6-403a-909f-bd3994dffbea)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/c54410f5-ce87-4ee9-b17d-820ae292639c)
 
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

![WhatsApp Image 2024-02-26 at 13 37 21_a8e7b5b7](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/7b40d124-a967-4b67-a022-98df4cafb565)

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

![WhatsApp Image 2024-02-26 at 13 37 21_a8e7b5b7](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/7b40d124-a967-4b67-a022-98df4cafb565)

 
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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/f32f53a4-808d-44f3-b4c7-dc4ada6b404e)
 
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
 
![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/a2447617-8253-4ada-ac5d-97d873f99927)
  
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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/fec56692-cb34-4b4d-963c-c037177ca14c)
 
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
 
 ![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/4fbe7ef1-dc7f-46fd-8f67-4ffd9ed5d282)

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

 ![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/40bd10d1-1c58-4ada-b250-ae1746957671)

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

![image](https://github.com/vijaygowdu/OS-Linux-commands-Shell-script/assets/147473788/ef639766-d760-449f-b367-783bb65b11c6)

# RESULT:
The Commands are executed successfully.
