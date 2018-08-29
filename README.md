# Qlaunch-Tutorial for 5.1.0 Text Editing
Note: This method is ONLY USED over LayeredFS with Atmosphere, I'm not responsible if stuff breaks on your Switch, this stuff is easily messed up and could result in you crashing your Switch on boot until you remove the LayeredFS files.


This is a tutorial of doing simple text edits on Icons using Kuriimu's editor to edit the .msbt files, Uwizard to decompress and recompress the .szs archive files.


Step 1:
Grab Uwizard and Kuriimu from this Github.

Step 2:
Get your own unedited qlaunch extracted from your 5.1.0 System Partition or use the one I have linked in the Github (the file called 00)
If you want to get it from your System Partition, it's under Contents/registered/8684b0ddab1581d300a15ebc96c6bf2c.nca (only on 5.1.0)

Step 3:
Use Hactool with the proper keys to extract Qlaunch (the 00 file) into a romfs folder, use it as a nca file to extract, not NSP.

Step 4:
Go into the extracted romfs folder under message, USen, there you'll find qlaunch.msbt.szs and setting.msbt.szs

![Step 4](https://i.imgur.com/zYzjcsr.png "Step 4")

Step 5:
Open up Uwizard and go to the Archive Manager tab

![Step 5](https://i.imgur.com/rniejd2.png "Step 5")

Here you'll see Decompress SZS and Compress SZS, don't worry about Compress for now.
Click on Decompress SZS and open either setting and or qlaunch, then save it as a .msbt file for editing in Kuriimu.

Step 6:
Once you have the .msbt file saved, open up Kuriimu.
Click on File, Open, find whereever you saved your .msbt file and open it.
Then you'll see a lot of entries on the left like so.

![Step 6](https://i.imgur.com/WpUPA4J.png "Step 6")

Find whatever you'd like to edit, and change the text to whatever you like (Keep in mind that this could break certain texts)
For example: In setting.msbt, under SetCnthardware_BodySysUpdate, you can change the Current Version that shows for the Switch, like how it shows 5.1.0, or whatever, you can edit it to whatever you like. 

![Step 6](https://i.imgur.com/45vM5m5.png "Step 6")

Once you are done editing, click on File, Save at the top.
Now, go back to Uwizard and click on Compress SZS.
It'll ask you to find your .msbt file you edited, double click on it, then save it as for example setting.msbt.szs (make sure the other one is deleted else it'll throw out an error saying it's already there)

Step 7:
Once it's compressed, it should be compressed as a .msbt.szs file, if not double check and make sure you compressed it correctly.

Step 8:
Using Atmosphere's LayeredFS, make a folder under atmosphere/titles called 0100000000001000, this is the TitleID for QLaunch.
In that folder, make a file called fsmitm.flag, this is required to be able to edit QLaunch over LayeredFS.
Make another folder called romfs, this is where you'll be putting your modified QLaunch files you just made.

![Step 8](https://i.imgur.com/GZWBZiB.png "Step 8")

Step 9:
Under romfs, make another folder called message\USen, here you'll put your modified .msbt.szs files you just made in Kuriimu.
Once you've done that, you're done! You should have edited QLaunch text now, make sure to reboot your Switch back into Atmosphere and double check and make sure that the edits you've made are indeed working.
![Step 9](https://i.imgur.com/2EXeWu5.png "Step 9")

