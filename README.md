# heartbleed-ubuntu-fix
A shell script to fix the heartbleed issue on Ubuntu Servers


There was a major vulnerability found today called shell shock. You can read more about it here:

http://www.pcworld.com/article/2687857/bigger-than-heartbleed-shellshock-flaw-leaves-os-x-linux-more-open-to-attack.html

To test if you have the problem you can run the following command from the shell command line:

env var='() { ignore this;}; echo vulnerable' bash -c /bin/true

-----------------------------------------------------------------------------------------------------------------

If Vulnerable it will print vulnerable like this:

root@ip-10-40-6-208 /home/ubuntu
  # env var='() { ignore this;}; echo vulnerable' bash -c /bin/true                                                                                                                                   !1501
vulnerable

------------------------------------------------------------------------------------------------------------------


If ok it will print an error like this: (which is a good thing)
root@ip-10-144-78-102:/home/ubuntu# env var='() { ignore this;}; echo vulnerable' bash -c /bin/true                                     
bash: warning: var: ignoring function definition attempt
bash: error importing function definition for `var'

------------------------------------------------------------------------------------------------------------------
