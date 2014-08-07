To use threads perl (like Trinity) at Beocat, you need to install perlbrew.
Here is the link showing how to install it: https://support.beocat.cis.ksu.edu/BeocatDocs/index.php/Installed_software#Perl

I just followed steps of the link. 

Briefly,
-To setup perlbrew, change your shell to bash

		$ bash
	
-Install perlbrew

		$ curl -L http://install.perlbrew.pl | bash

-Make sure that ~/.bash_profile exists

		$ ls -l #at your home directory, then you could find it
		
-Add source -/perl5/perlbrew/etc/bashrc to ~/.bash_profile, and then source tour bash profile

		$ echo "source ~/perl5/perlbrew/etc/bashrc" >> ~/.bash_profile
		$ source ~/.bash_profile

-Now, install perl with threads within perlbrew.  Before that, find current Perl version 

		$ perl -version
		my one was perl 5, version 16, subversion 3 (v5.16.3)
		
-My case the version is 5.16.3, so you run

		$ perlbrew install -f -n -D usethreads perl-5.16.3 #It tooks quite a long time, so just wait until it's done.


-To run thread perl, you should add "perlbrew switch perl-5.16.3" at your shell script. 

