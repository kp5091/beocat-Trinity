Downlaod installation file and Install Trinity
===============================================
To get Trinity installation file, go to: http://trinityrnaseq.sourceforge.net/#sample_data

You can download the file using wget or directly your download folder of your computer.
In my case, I directly downloaded the file into my computer, then I transfer it to my directory where I want to deposit by using CyberDuck.  

-You need to untar compressed installtion file at the directory where you desopit the installation file. 

		$ tar -xvf trinityrnaseq_r 20140717.tar

-You will see new directory "trinityrnaseq_r 20140717" at current directory.

-To install all software for Trinity, type "make" at trinityrnaseq_r 20140717 directory

		$ make #You will see many lines showing step where you are


Now, you need to install perlbrew to run Trinity with your NGS reads at Beocat. 

If you run Trinity without perlbrew installation at Beocat, you would get error message: Trinity line 5. (which is "use threads;" in Trinity.pl) 

