# pinject
C++ Process Injection

This code will search thru running processes to find the pid of the desired process you wish to inject in to and will create a cmd.exe thread within that porcess. It uses msfvenom gernerated shellcode windows/x64/exec cmd=cmd.exe exitfunc=thread. Shellcode can be replaced with whatever shellcode is desired. Code is currently set to find winlogon process. You will only be able to inject into winlogon if you are running in a SYSTEM context or you are combining this as the injection payload after performing ACL editing on the winlogon process as part of another exploit. You can change the process to another target process that you have permissions to inject in to.

![image](https://user-images.githubusercontent.com/84335647/209874459-4f095b72-1fdb-43eb-b9e6-1a82ea441422.png)


Resources I used to help figure this out

https://www.ired.team/offensive-security/code-injection-process-injection/process-injection

https://github.com/Nero22k/Process-Injections-Techniques

https://stackoverflow.com/questions/30254793/getmodulefilenameex-split-output
