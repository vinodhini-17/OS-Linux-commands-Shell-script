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
.
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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/9527293b-cc2e-4e59-be01-26d385f8abb7)



cat < file2
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/fd327f3e-6c15-450f-9eb1-77ca2aa5bba7)

# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/ac5437ed-262e-4f2f-9d97-31fb0488f0ff)

 
diff file1 file2
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/3f75c1fa-ae88-4f28-b19a-6d29819b63ac)


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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/44519a0a-3889-41ce-9709-e8446990fdf4)



cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/78cc777c-dcd0-40d2-a89d-1b12fe855ed5)

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



grep hello newfile 
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/ea003b4b-badb-4811-a77c-6af1bcc4802e)



grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT



![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/768e0b5c-09d9-4cbe-9090-220682a79318)

cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/f613eb46-b31d-437a-83d1-d3c7ddfc8eaf)


grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/51d110b0-ff98-4fb6-99e8-b0c49756e9c4)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/39c04425-42a7-47a6-8a9c-011d622017ec)
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/c13f2238-dc7e-4290-9f66-8858e7912a8d)

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

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/72903c08-8860-44b8-a045-753fd542fbe8)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/d2c9dc09-2ca8-4464-b64f-6986d0f84195)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/0c008ac2-79cf-4c93-8178-fe634034c12a)


egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/6f4fde9f-b35c-4261-b9cb-349e658bb46b)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/c3109f3b-a41d-4c05-95f1-8a145ae798df)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/eb2d7273-7bda-4844-87c6-61e671e32e97)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/74d70e68-4ceb-4902-aeb5-4e47d7c3361c)



egrep '[1-9]' newfile 
## OUTPUT


![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/b928ddd8-31e9-4ebf-b32d-b1ef86f9d5ea)

egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/a8f5ee4a-01ef-42eb-9c0e-9a7c08db79f5)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/601a9900-2c7a-441b-9f1b-0220a9a50d36)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/6baf6323-1747-414f-b193-34fb38c5e96a)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/f85f4299-c345-47fe-b83b-d2296a69111a)


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

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/db2c7c88-b72d-4290-b026-f983816e6d4a)


sed -n -e '$p' file23
## OUTPUT


![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/4874aa8b-8d90-4850-8d9f-1484e90b9f42)

sed  -e 's/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/42f74754-19e1-4b2c-b8c4-40a92dc2b78b)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/e24ac431-fd4d-4192-8881-e70f8e181883)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/53222482-435f-4298-95d0-04b7f03f24e5)




sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/535d8c66-33e6-4ff2-8013-2f6a7405f152)



sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/3c15e665-be15-4f02-b4fb-c03b1edd2b78)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/e91ada81-27d6-4481-8d20-9eb1fbbd9062)


seq 10 
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/2ad19e40-3d8f-499b-8d67-82c0e6881347)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/58710804-62d4-4cab-875a-87903d6421c8)


seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/d31ea1ec-1891-4e20-9b6c-00a1ba4fba6a)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/15111ca0-52ba-430c-bf4d-0bd7efca40cd)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/a564cd28-51fd-4d6c-9619-1c973a0d1a65)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/c6cbf457-87b0-4eea-a989-bad42d43d58e)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/030d3483-136c-4325-a4a1-f0a0e6d5dfca)



sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/9a10405e-ef5a-4913-a12e-d6993d21c4a8)


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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/18045965-fbf3-4581-8d43-a304fc661aa1)


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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/90d64c67-a5a6-4e03-831b-2739da7aae9d)



#Using tr command

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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/27fb9db5-91d7-4945-bbf8-df262808d09c)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/87922565-70be-47b6-83a1-1077995a3e02)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/f16eb0a4-0113-40ae-889e-4dea182dcc4f)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar



tar -xvf backup.tar
## OUTPUT

gzip backup.tar
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/60be24fb-cb04-433d-aab7-89fccb0612a5)

ls .gz
## OUTPUT
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/4e31517b-c916-4f3c-b9ff-2e6f5ae40184)

gunzip backup.tar.gz


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/eff54a39-92bd-4b70-bf32-7bd42fd6b792)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/53750688-25a7-4e90-a338-f8a81dc4c115)


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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/28f7300e-c9a4-4af7-8919-4e0e396bad25)

 
ls file1
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/8a7fec8a-019e-4a79-9382-924c26d5ec46)


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/7e50e3cb-974d-4ad2-b27a-598a5738e115)

abcd
 
echo $?
 ## OUTPUT


 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/5a969d73-5ec0-4abd-927d-d25a1630660e)

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

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/8eef7169-38cb-44f3-bf1e-58b9faed2056)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/47201b18-a6ed-4b07-965f-78861ae9bc4a)


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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/e55c1757-ae69-4ba3-809e-fb5e1c216164)


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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/521905c5-4d38-4c40-8462-2d9341094bcd)



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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/6b020f36-a7a8-4f20-8fdf-17c1c90f034c)


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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/2b4defa8-b71b-4c4e-8a8e-e98527eeda3f)

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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/19487ff6-2f22-4538-bebf-51d9882d9101)



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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/828f949b-2813-4c24-8d88-dfea813ce536)


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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/58141fd8-54c8-4a54-928c-ad2f9c0aa890)

 
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
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/d44f451a-81cf-4771-965c-dc26b9c5e2fc)

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
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/ca3dceb2-5ca2-4edc-9658-7b1fdc327549)

 
 
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
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/aa5d7a6f-ce47-429b-a1e2-ab8545f84934)

 
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
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/286c1d66-c6e5-46f0-aff9-940e7d30d2a7)

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
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/83e06405-8bd3-46a6-86d9-b5d4f9850c35)

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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/a92285c3-5d98-4c7e-8636-06d4402522d8)


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

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/e444b8c1-fc18-47ec-a45f-effba6072d27)

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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/23f38d0d-0bd8-49f9-a8f1-753d962a2070)

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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/04714a39-0c4c-4e84-b444-b4f6048d2d8d)


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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/b3ed61fb-4b8a-4db1-8c7e-4ba527746428)

 
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
![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/7e4af8ce-eaf2-4b87-8d6d-659ce4d7aaec)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/5a848867-0367-4578-ad8b-b9435035086e)

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

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/92e205e9-165b-4125-b26a-35a07b625d36)


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

 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/c704fb52-33db-4a45-af1a-e122da657221)

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
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/d9d1d8eb-1d12-4a6c-8c9d-660c532b17d0)

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
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/c872022b-2182-480c-80cf-4a7b64465925)

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
 
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/2af97455-b253-4a79-8625-d467886dd9ef)

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
 ![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/9a06b41b-e748-44f4-8dad-3bc766523e36)

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

![image](https://github.com/vinodhini-17/OS-Linux-commands-Shell-script/assets/145742741/213ddba5-6ece-4f60-9970-f6d5ebfc2e87)

# RESULT:
The Commands are executed successfully.
