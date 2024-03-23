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

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/5d7ac0d0-0a2f-4e00-9a9c-0063e3ec94fd)


cat < file2
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/4356727a-7ad1-4f49-9962-7c0a81ec99d1)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/786c4c27-ab76-4976-9c82-0d591498f099)

comm file1 file2
 ## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/795b808b-cf6e-44b3-b8ee-7512e86dee31)

 
diff file1 file2
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/e63add40-a5a8-42e5-916c-1f5a68d64668)

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

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/6e8612a5-f79e-4ccc-b7c8-299071c07bee)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/6fc10271-e49c-47fe-9571-73e7d3285191)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/3102e6bc-6274-4682-a244-9eaebcca2b00)

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

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/5f51b5cd-b244-4f94-873e-55fc9ff16596)


grep hello newfile 
## OUTPUT


![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/45dbd0cb-ba1e-47b8-bc68-55324846f3b2)


grep -v hello newfile 
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/1f778c88-df6e-4e27-8ef1-bf2233fcc274)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/4078c41e-c127-4871-9b27-e06c07604d9d)



cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/7e33b81b-5433-4685-bda4-e25907f8eb1e)


grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/8a8b09f7-97b4-4721-bc42-8c80c3d99009)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/ac9ecf96-b925-4c6b-bf86-aefcc635665f)

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

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/142ccc55-f0a2-4922-97e5-2129424138c9)


egrep -w '(H|h)ello' newfile 
## OUTPUT


![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/d91e61c1-4135-48a7-a6af-b2faed2e2da4)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/340150f8-8f19-4d93-95ff-ae4c31214e83)


egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/3a7c4bef-03dd-4f5a-9d88-743b5269bda0)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/704f941f-08ce-4f9f-9e73-fe08dcccb52b)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/d012abcd-6a09-4137-8ed0-cbb4dcabd2e8)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/92da5fab-5047-46a9-be84-a728bc35f267)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/8328641f-4146-4582-96d9-bef01b0bd5c9)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/d9c5ff96-495e-4f18-9ed3-3a5678b50746)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/47bf5494-32bc-4fa2-ab5c-814b642dd11c)

egrep l{2} newfile
## OUTPUT


![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/ee084f06-89bd-4383-bd22-53c71a98fb81)

egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/0f6c4117-098d-486f-86f0-88a7eba456ee)


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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/9f563cf0-7b4b-4855-a6e8-a6fe7575afae)



sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/b97802ad-13b7-40cc-89a7-72531dfa8680)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/556f9328-05b7-49f6-b1e9-ef3d03db2e0f)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/946536e2-4a3c-4c47-81a5-51a927c9a299)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/7362ebb4-577c-4a8f-95a2-474347310bfc)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/301f1bff-06aa-43f9-b789-6b5201f77aa6)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/c2ae0cd8-ef4f-402e-9ee6-7b80fc6d0164)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/dab0d6e2-7057-4103-bab8-d02ed71f4eb0)


seq 10 
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/a8fe1f03-299a-417b-b4e8-887b2ea4955d)


seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/8f3eb0bd-8a02-42bc-845c-29373b9417aa)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/4cba6ff5-34a1-489c-b402-abfc7065e20e)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/968066bf-ef9e-422d-a0bc-023c458796dc)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/220d9cf1-fb88-4486-9af7-a4cc8ae0929c)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/112a7e50-31e0-490b-a33f-8c7d59e16bb4)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/5cc92470-7591-4e5e-81da-0b7aa6e47ef7)



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
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/451a9c6d-a27b-46d2-a058-835fa494ab9f)


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

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/68c42cb6-30b0-457b-9849-a808cb4fb50d)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/6fab4fd2-874b-4f0e-a474-7dfcf32a1706)

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

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/807f7e12-a18b-42d2-b21e-4817edb74d52)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/cd7fd71e-0b28-426c-9753-33d9eea0d68b)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/b0a1356d-2d4f-4962-b9bd-557bc461c6d1)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/262e9cd9-c1c8-4610-bbc8-7a3a26897709)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/2fb1ec34-eb89-4868-9b46-dfd90c10ba81)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/3beacfdd-82a5-4b0b-99ef-be17f1fc6ace)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/e4c70947-833c-42ba-861f-c3c2f6987296)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/a60547ec-17e7-4d93-86b0-4bb380e1ceb3)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/cc49ec96-834e-409f-85b8-ec7c2407c923)

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

 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/06d84cca-93d9-4017-bf9f-d55e52a0158c)

ls file1
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/abd54a75-6c62-4e36-8a2f-c3242db432ae)

echo $?
## OUTPUT 
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/6f4ddb1c-3f2a-44c9-909b-c0400cb456d3)

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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/a2000a3e-fdf3-40ac-a00b-c62126ad1c5c)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/113eb8d5-28f7-4c1d-b9bb-6f8b8ae360c1)



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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/562503b2-7eb7-40a2-8bba-b13f0bd09e7c)

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

![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/cd806e3b-e1b9-46a1-98a3-c19e844b8246)


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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/b2efd1b2-4c6d-4c4c-b83a-59659849fa8e)


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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/bcec2b89-46fc-47bc-8434-4819b4de98d2)

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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/5b66c88d-d0fe-4c63-bd40-adf41afebb00)


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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/19af9432-a20e-49c1-a615-48d819f295ef)

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
 ## OUTPUT
 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/a3cff0a8-2017-40b1-9d0f-466155be5aca)

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
 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/62c1da6a-30dc-4934-a720-48b0c84da8a1)

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
 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/a820ef45-5f4a-4eb6-9dfd-8a1f5d09a1e3)

 
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
 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/5d08baec-6a3d-4e2b-9d45-fe908181874c)

 
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
 ## OUTPUT
 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/9cf67ddb-95a9-455a-9aef-e7a222d592a2)

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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/96a08af7-7228-4885-a9c4-bd9a6452000c)


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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/2bfa2cbc-6439-46ae-a875-b55f8cac34d9)

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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/d125c8f1-fc9d-4872-997d-d7a5d8469127)

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

 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/de16b33c-5244-46d3-b88b-2caf0b2b0f8d)

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
 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/fa01fe15-bb03-4f7f-8d71-c6d8f0be0394)

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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/f7724b27-07a0-4b87-b166-0cb144b56dc3)


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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/a557f192-199a-4912-950b-d9e241fffde3)

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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/47835a09-bf81-4c7f-8867-b52f332566e3)

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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/e2f9aa2e-c4ad-4cbf-8336-c2c989ebf3ab)

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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/84368ce2-e71d-4315-8376-3cae953bdc46)


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
 ![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/5746e8e7-4737-4691-b067-e0cf11197a72)

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
![image](https://github.com/IMRAAN2005/OS-Linux-commands-Shell-script/assets/149347407/a643df57-d1b9-41c4-9168-5bf486cbdd45)


# RESULT:
The Commands are executed successfully.
