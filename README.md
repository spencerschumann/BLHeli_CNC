# BLHeli_S CNC

This is a fork of BLHeli_S for use as a CNC spindle motor. 

The most significant change compared to standard BLHeli_S is
removal of the arming sequence. Careful! Use this at your own 
risk, and the author is not responsible for any damages this may
cause!

The reason for removing the arming sequence is that CNC machines
typically operate in open-loop fashion, blindly following G-Code
instructions, and they can't listen for arming beeps to know when the
procedure is complete. Failed arming results in the spindle not
spinning up as expected when commanded, which then leads to job
failures, broken bits, etc.

The other change compared to standard BLHeli_S is a simplified
startup procedure so that the spindle can spin up as promptly as
possible when commanded, even if that happens shortly after powerup
or following any ESC resets that could occur, for example, due to
signal or power glitches. The following simplifications were made:
* Supports RC PWM only, rather than auto-detecting oneshot/dshot/multishot
* Removed startup tones    

Spencer Schumann<br>
July 2022

---
## Original README below:
---

This tree contains BLHeli code for sensorless brushless motor electronic speed control (ESC) boards.  
  
To view and use the files, click the "Clone or download" button on this page,  
and then select "Download ZIP" to download the repository to your computer.  
  
For flashing and configuration, download the BLHeliSuite PC software:  
https://www.mediafire.com/folder/dx6kfaasyo24l/BLHeliSuite  
  
For more information, check out these threads:  
https://www.rcgroups.com/forums/showthread.php?2640796 (for BLHeli_S)  
http://www.rcgroups.com/forums/showthread.php?t=2136895 (for BLHeli)  
  
And look in the "BLHeli_32 ARM" folder for info on BLHeli_32.

October 2018,
Steffen Skaug
