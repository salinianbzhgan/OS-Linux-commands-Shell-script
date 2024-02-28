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
![Screenshot from 2024-02-26 17-57-58](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1bdb3770-9271-4b8e-b346-b8f8e1a53144)



cat < file2
## OUTPUT
![Screenshot from 2024-02-26 17-58-14](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/61b310e5-7608-4622-91e5-7b9d0af2261f)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2024-02-26 20-30-46](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/260e9a26-daf4-4cb6-9e02-f69e6dfc3083)

 
comm file1 file2
 ## OUTPUT
![Screenshot from 2024-02-26 20-31-06](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/b09ff117-6980-4d02-b628-a77150e0f4ac)

 
diff file1 file2
## OUTPUT
![Screenshot from 2024-02-26 20-31-22](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/5251f892-9027-44bf-af07-02241eb043ea)


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

![Screenshot from 2024-02-26 18-08-42](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/19019426-9add-4325-a0b0-a67fb8a87bac)



cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2024-02-26 18-08-59](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/db137cbe-e608-4468-97f8-51d2305adeda)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2024-02-26 19-01-36](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/b4b07843-e36c-4737-a709-59b8c930390d)


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

![Screenshot from 2024-02-26 19-03-33](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1ec96c20-54c5-49fb-8a19-f70b7a71acf1)


grep hello newfile 
## OUTPUT

![Screenshot from 2024-02-26 19-03-47](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/584edc18-3df2-41e6-8933-9877df6fb419)



grep -v hello newfile 
## OUTPUT
![Screenshot from 2024-02-26 19-13-21](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/85888f5b-2ade-4abe-9113-fde4777fea93)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2024-02-26 20-36-27](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/91205458-5156-440b-9444-0bc108736fe7)




cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2024-02-26 20-36-41](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/b995cb68-4837-4b90-bbd3-a041251b09ee)



grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2024-02-26 19-26-26](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/a182b65c-e490-481d-8651-7805c6016065)
![Screenshot from 2024-02-26 19-27-14](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/4c07b221-20b2-48dc-af6e-3baf5e8fd6e7)




grep -w -n world newfile   
## OUTPUT
![Screenshot from 2024-02-26 20-38-38](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/221a8f86-c750-4b38-8803-6ae92561b40d)


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
![Screenshot from 2024-02-26 20-39-31](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/2ce96eb6-2c1d-4130-8177-36c72204d4c8)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-39-49](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/d9c55353-f693-4c5a-9196-56b1e638c70d)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2024-02-26 20-40-32](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/5cc99df9-9ad4-43a4-9030-6b3aad9f7e5f)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-42-55](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/7abead62-7c71-4d41-bd2a-e4d4e7e12ac8)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-43-27](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/95e9b839-7542-4e53-a507-e6cd0054b6f3)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-43-39](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/ec482880-e249-48e8-ac55-50f1f9c07053)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-44-03](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/a632e0d5-baf2-446b-9cfb-5fc6c51eec69)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-46-28](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/bceddd37-18b7-4bd6-b6b5-0f8904620ae7)




egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-46-42](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1299dc45-9ad2-4087-ae6f-7561d75d1aeb)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-46-56](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/6f4fbdd6-04e5-448c-bec8-0a7fd2cb3ccf)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2024-02-26 20-47-08](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/bec38463-f408-4385-8e8a-d28514175321)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-02-26 20-47-22](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/aeea5d6b-b6b1-4175-9b94-a5e1f82776ae)


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
![Screenshot from 2024-02-26 20-48-24](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1b7546dd-596e-4cc4-9aae-53ebc4636eff)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-02-26 20-48-53](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/169da9aa-3f98-4d1f-b6d5-e6338cc4c3f2)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-02-26 20-53-11](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/f89ee6d2-5d92-42f4-9ef9-f2bb57050d04)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-02-26 20-53-44](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/27e67823-b4f9-43fd-a2fc-eb54d0d6c546)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2024-02-26 20-53-53](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/db23ef47-5a38-417a-a620-f6d5598a3686)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-02-26 20-54-04](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/a93df0ae-cbe4-46c0-ac44-7217227253a9)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-02-26 20-54-12](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/645f11b8-3e99-4599-91f0-50a89c2f4e3d)



seq 10 
## OUTPUT
![Screenshot from 2024-02-26 20-54-26](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/4cb9b75a-ec3c-4216-b7d8-d5a3d67b5d85)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2024-02-26 20-54-35](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/7914a12e-b7b1-42f4-923e-b4f715a36f07)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2024-02-26 20-54-44](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/01c1d38f-0ba7-433d-92bd-60013176a2a0)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2024-02-26 20-54-55](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/bbc211c0-d81e-4aa0-a002-2f8fdf72edc8)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-02-26 20-55-14](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/2fd7dabb-3a33-402b-b274-e946d898363e)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2024-02-26 20-55-56](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/be433db7-2343-4436-b232-10968325170d)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2024-02-26 20-56-05](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1189b83d-9b54-49cd-9442-64d22a9f2db3)


sed -n '2,4{s/$/*/;p}' file23

![Screenshot from 2024-02-26 20-56-15](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/b71359ac-630a-40d4-a15d-5973024d77e4)


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
![Screenshot from 2024-02-27 14-21-17](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/08fbcf0e-bb74-4575-a871-ff48681d7c05)


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

![Screenshot from 2024-02-27 14-23-58](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/e8d5c15d-87f1-4b40-9471-8154033e24a5)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-02-27 14-24-48](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/c541042b-fd64-4627-92bb-404348cb58ca)


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
![Screenshot from 2024-02-27 23-16-56](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/ca5ca548-1615-4722-8b10-798b67b3aa44)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2024-02-27 23-17-16](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/15f10989-43de-4a57-8cc9-9c392d2da006)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2024-02-28 09-14-58](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/259c0abf-768e-48f6-8bae-bafa2ead1d13)
![Screenshot from 2024-02-28 09-14-46](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1db6ecf0-952a-4458-ac16-13d028e470cc)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2024-02-28 09-14-29](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/eb67e3f4-449a-478a-b49f-e148c25fffd6)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2024-02-28 09-14-14](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/7c159732-71bd-43bc-b922-3e43f299dbc4)

gzip backup.tar

ls .gz
## OUTPUT
 ![Screenshot from 2024-02-28 09-14-01](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/d3cbe499-85e2-4cb3-880c-61d0a465c081)

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
![Screenshot from 2024-02-28 09-13-52](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/73ddccad-cc40-4fc8-afcb-b73827fb9067)

 
cat << stop > herecheck.txt
![Screenshot from 2024-02-28 09-30-57](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/3d50e917-661e-438b-8638-6c5f12438e95)

```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot from 2024-02-28 09-13-22](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/7ffd0fbf-818d-40f5-884c-6b2886d503f9)


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
![Screenshot from 2024-02-28 09-13-01](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/2d050dc9-f837-48a6-b716-8061160a82e2)

 
ls file1
## OUTPUT
![Screenshot from 2024-02-27 23-23-12](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/c3007567-0506-4bfc-a8f0-ad8bf97b56ad)


echo $?
## OUTPUT 
![Screenshot from 2024-02-27 23-23-20](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/10c8cf9a-7af7-439b-9db6-134fd9ddbb62)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT:
![Screenshot from 2024-02-27 23-23-02](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/6aa98a7e-0447-43d9-a5fb-1d12a01ed2dc)

 
abcd
 
echo $?
 ## OUTPUT:
 

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
![Screenshot from 2024-02-28 09-12-40](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/18301fcf-f06c-4af5-8b40-4123b798c3fa)


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
![Screenshot from 2024-02-28 09-12-24](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/20b022a3-f901-402e-b7be-1f84547c95bc)

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
![Screenshot from 2024-02-28 09-12-13](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/5864b689-5cdf-4e92-8995-a6775f87661a)



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
![Screenshot from 2024-02-28 09-11-58](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/11229923-1c17-49db-925f-63a8bcb36e48)


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
##OUTPUT:

![Screenshot from 2024-02-28 09-11-45](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1773429f-2148-4daa-bbb1-ed0061121d83)

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
![Screenshot from 2024-02-28 09-11-34](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/3495aa88-9f7d-49bf-9d02-700e65122127)


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
![Screenshot from 2024-02-28 09-10-38](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/7115d1bc-4e90-4bda-b6a2-8e230f0c4130)

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
![Screenshot from 2024-02-28 09-10-24](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1a93aab7-eb80-4df2-92f7-6eddd666ac9f)

 
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

![Screenshot from 2024-02-28 09-37-14](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1594fbf2-2909-47c5-89fa-a8c8b3b6df03)

 
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
 
 ![Screenshot from 2024-02-28 09-37-29](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/235623eb-908f-423c-a8fb-ca126f1f7746)

 
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
 ![Screenshot from 2024-02-28 09-37-37](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/d57bc488-d233-4493-a9ac-c2aadc308493)

 
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
 ![Screenshot from 2024-02-28 09-37-47](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/4747251a-417b-4982-8c97-f554621fe0c7)

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
 ![Screenshot from 2024-02-28 09-37-56](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/a22a7562-a237-4831-8556-153ae63aed57)

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
![Screenshot from 2024-02-28 09-38-10](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/aca60b75-d68f-4a06-a975-0c81aa3256d9)


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
![Screenshot from 2024-02-28 09-54-14](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1fd8d603-3a59-43f2-93a7-5fcfdd851879)

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
![Screenshot from 2024-02-28 09-38-51](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/d8a153be-8fd8-4f05-8315-5b0037699557)

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
![Screenshot from 2024-02-28 09-39-03](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/970d1006-c533-47f3-a6f1-71cc1c20b4d1)

 
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
 ![Screenshot from 2024-02-28 09-39-03](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/076b54cb-b88a-440e-807a-6d5a6f8fec73)

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
## OUTPUT:
![Screenshot from 2024-02-28 09-06-47](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/42720262-e968-4e49-b1b5-731183ee6c5a)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT:

$ ./exread1.sh 
![Screenshot from 2024-02-28 09-06-47](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/ba27bdc2-c842-49b2-a944-2ebfd688ab03)

 
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
![Screenshot from 2024-02-28 09-02-11](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/4d03f839-cad6-4474-b50b-74f1d748b855)

 
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
![Screenshot from 2024-02-28 08-59-41](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/a1aed1f3-7820-49b1-bd8e-3bb0f6da42f6)

 
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

![Screenshot from 2024-02-28 08-59-41](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/6d906edf-8d90-468d-9f93-017f6aa03345)

 
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
 
 ![Screenshot from 2024-02-28 08-53-50](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/1151be21-f597-4a26-a6b8-96430f2bfefa)

 
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
## OUTPUT :

 ![Screenshot from 2024-02-28 08-46-56](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/6f668782-9f0b-43b1-af8e-68479a42f589)


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
![Screenshot from 2024-02-28 08-44-48](https://github.com/salinianbzhgan/OS-Linux-commands-Shell-script/assets/145742862/79087e99-2129-4241-9a1c-409685cef2b0)


# RESULT:
The Commands are executed successfully.
