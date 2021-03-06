# Th3BlackHand

<p align="center">
  <img src="https://media.giphy.com/media/LLxAlFgptpskFCxyor/giphy.gif" />
</p>

What is Th3BlackHand?  
A python script that locks your laptop/pc screen if you forget to lock it, using an android application that is connected to the firebase database. This tool can be useful if you work/live with nosy people 😅!  

----

![Demo](https://media.giphy.com/media/TEcWMqTQqdBkKsbuZf/giphy.gif)

* As you can see in the above GIF, the tool keeps locking the screen, this happens because the value in the firebase realtime database is changed to False .. When you are not around your laptop/pc just change the value in the database to False using your mobile phone ;) 

--- 
<img src="https://i.ibb.co/5Kts11C/android-1.jpg" width="150"> <img src="https://i.ibb.co/TMdBYhM/android-2.jpg" width="150"> <img src="https://i.ibb.co/swKCDJd/android-3.jpg" width="150">


* You can fine the android project in the [Releases](https://github.com/inurlx/Th3BlackHand/releases)  
* Unfortunately you gotta modify the android project with your settings and build it, to get the APK FILE :) 
---

* Why should you use this tool?  
>> 1. Keep the nosy people away from your computer :D
>> 2. All you gotta do is just run the tool ONE time manually and it will configure itself in the startup applications and work in the background processes  
>> 3. You will not see any command prompt popping out of nowhere !  
>> 4. How to check if the tool is working or even kill it ?  

>>> ![Alt text](https://i.ibb.co/FmM0wHV/3.png "Check if the tool is working")

>>> 3.1 Go to Task manager > Background processes > Python  
>>> 3.2 Type the following command in the CMD/Terminal: tasklist /v | find "python"  

---

* Required Libraries ?
> getpass  
> os  
> socket  
> time  
> ctypes  

install the above libraries using the following command : pip.exe install [library name]  

!! If you face a problem installing Crypto Just install the following libaray instead: [pycryptodome] !!

NOTE: 

While trying to install the libraries: 

Please delete the following code block from Th3BlackHand.py

CMD = ctypes.windll.kernel32.GetConsoleWindow()      
if CMD != 0:      
    ctypes.windll.user32.ShowWindow(CMD, 0)      
    ctypes.windll.kernel32.CloseHandle(CMD)

----

* Python version?  

> Python 3.7.5  

---

* How to install the tool?    

> 1. Download Th3BlackHand.py   
> 2. Modify the code with your Laptop paths such as the python3 compiler path.  
> 3. Modify the link of firebase realtime database with yours !  
> 4. Import 'test-ed516-export.json' to your firebase realtime database .. just to save you some time :)  
> 5. Run Th3BlackHand.py using the Python3 Compiler!! <make sure to install the libraries above FIRST!>  

---
---
* Firebase Realtime Database Rules  
{  
  "rules": {  
    ".read": true,  
    ".write": "auth.uid === 'Your Account ID here'"  
  }  
}  

---
* Credits: 
> The Font-end / user interfaces were designed and coded by:
>> Osamah Saeed - https://github.com/OsDroidi

---
* Stuck on something? 

> open a new issue ;)


