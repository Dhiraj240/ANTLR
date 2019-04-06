# ANTLR

This repository contains the gist of antlr language, together with its usage and installation in windows in much simpler version.It contains one stop coverage in limited time.  

# Windows User

ANTLR is written in java.One must refer to [ANTLR](https://www.antlr.org/) just after implementing the following instructions.

## Step 1

Install ```antlr-4.7.1-complete.jar``` and store it in ```C:\Javaantlr``` you can give any name instead of ```Javaantlr```.

Add Environmet Variables to get it running on your ```cmd```.If you see ```CLASSPATH``` under System Variables append it with 
```C:\Javaantlr\antlr-4.5.3-complete.jar;``` If you do not have a CLASSPATH variable defined, select **New** and then enter CLASSPATH for the Variable Name, and ```C:\Javaantlr\antlr-4.5.3-complete.jar``` for the Variable value.

## Step 2
Now we need to create the batch files.

1.Create a new file in ```C:\Javaantlr``` called ```antlr4.bat```.
2.In this file enter ```java org.antlr.v4.Tool %*```.
3.Create a new file in ```C:\Javaantlr``` called ```grun.bat```.
4.In this file enter ```java org.antlr.v4.runtime.misc.TestRig %*```.
6.Save these files.

**Why we created ```.bat``` files ?**

1.The set of instructions written in batch file is a batch script.Its instruction is executed on the command line in a serial fashion.
2.Its extension can be ```.bat```, ```.cmd```, ```.btm```.
3.Now when you call ```antlr4``` on your ```cmd``` or ```powershell```, it will execute the command ```java org.antlr.v4.Tool %*``` without actually making you type the command written inside the ```antlr4.bat``` file.
4.You simply type your filename here ```antlr4``` it will execute on the command line interpreter with the following outcome.

![antlr4](/screenshot/1.png)


5.You can see ```java org.antlr.v4.Tool``` instead of ```java org.antlr.v4.Tool %*``` in the above screenshot.It is because ```%*``` is used to pass all the arguments because of which you are able to see several extra outcomes of it.

6.Similarly you can check the execution of ```grun``` on ```cmd```.

![grun](/screenshot/2.png)

```
Note : It is recommended to use Power Shell instead of Windows cmd because it provides administrator privileges which some commands need it.
```
