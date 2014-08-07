To use threads perl (like Trinity) at Beocat, you need to install perlbrew.
Here is the link showing how to install it: https://support.beocat.cis.ksu.edu/BeocatDocs/index.php/Installed_software#Perl

Perl

The system-wide version of perl is tracking the stable releases of perl. Unfortunately there are some features that we do not include in the system distribution of perl, namely threads.

Submitting a job with Perl

Much like R (above), you cannot simply 'qsub myProgram.pl', but you must create a submit script which will call perl. Here is an example:

#!/bin/bash
#$ -l mem=1G
# Now we tell qsub how long we expect our work to take: 15 minutes (H:MM:SS)
#$ -l h_rt=0:15:00
# Now lets do some actual work. 
perl /path/to/myProgram.pl
Getting Perl with threads

Setup perlbrew
Change your shell to bash
Install perlbrew
curl -L http://install.perlbrew.pl | bash
Make sure that ~/.bash_profile exists
if [ ! -f ~/.bash_profile ]; then cp /etc/skel/.bash_profile ~/.bash_profile; fi
Add source ~/perl5/perlbrew/etc/bashrc to ~/.bash_profile
echo "source ~/perl5/perlbrew/etc/bashrc" >> ~/.bash_profile
Then source your bash profile
source ~/.bash_profile
Now, install perl with threads within perlbrew
Find the current Perl version.
% perl -version

This is perl 5, version 16, subversion 3 (v5.16.3) built for x86_64-linux
(with 22 registered patches, see perl -V for more detail)
(...several more lines deleted)
In this case the version is 5.16.3, so we run
perlbrew install -f -n -D usethreads perl-5.16.3
To temporarily use the new version of perl in the current shell, we now run
perlbrew use perl-5.16.3
To switch versions of perl for every new login or job, run
perlbrew switch perl-5.16.3
You can reverse this switch with
perlbrew switch-off
