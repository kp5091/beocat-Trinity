To get Trinity installation file, go to: http://trinityrnaseq.sourceforge.net/#sample_data

You can download the file using wget or directly your download folder of your computer.
In my case, I directly downloaded the file into my computer, then I transfer it to my beocat account.  

-You need to untar compressed installtion file at the directory where you want to desopit. 

		$ tar -xvf trinityrnaseq_r 20140717.tar

-You will see new directory "trinityrnaseq_r 20140717"

-to install all software for Trinity, type "make" at the same directory

		$ make #You will see many lines showing step where you are


Now, you are ready to run Trinity with your NGS reads. 

