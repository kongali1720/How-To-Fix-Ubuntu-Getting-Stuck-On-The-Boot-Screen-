# How-To-Fix-Ubuntu-Getting-Stuck-On-The-Boot-Screen-

The operating system getting stuck at bootup is a bothersome issue as it prevents you from accessing 
any application on your PC.

I tried disabling file check during boot, getting into recovery mode, restarting gdm3 service, changing boot config to, 
but nothing seems to work. restored all the options in the menu later after pressing ok,I clicked alt-F2 and logged via
terminal entered these commands sudo apt upgrade and sudo apt update waited as usual.

I had some broken packages repaired them and removed outdated ones but eventually it worked.

Solution 1:

Try this:

Choose recovery mode.
Drop to root shell prompt.

Press Enter.

At the root shell prompt, type  journalctl --since today Look through the resulting journalctl log to find out 
what was happening just before your system got stuck on the last attempt.

Hopefully that can give more info that can be helpful. For example, it if turns out that it gets stuck initializing 
some particular service/package, you could try disabling or removing that service/package.

Solution 2:

I had same problem too, I am not quite sure how it worked but i feel it can work on you too. 

First i switched to recovery mode. restored all the options in the menu later after pressing ok,
I clicked alt-F2 and logged via terminal entered these commands sudo apt upgrade and sudo apt update waited as usual 
I had some broken packages repaired them and removed outdated ones but eventually it worked.


**A takeaway i learnt later ** someone suggested to me that in future if i want to switch to newer version of ubuntu 
it is more efficient to use Cl since it will do magic itself and overwrite the old reinstalling with release requirements. 
hope this helps.

Ubuntu 18.04: Boot Freeze / Purple Screen Hangs, Go to VM->Settings->Display and uncheck Accelerate 3D graphics. 
The Ubuntu VM now boots in normal mode and the screen resolution can be switched. Now to fix 3D acceleration,
you need to disable Wayland. Open up a terminal: sudo nano /etc/gdm3/custom.conf Uncomment the line …
