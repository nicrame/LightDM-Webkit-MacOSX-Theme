LightDM Webkit MacOSX Theme
===========================

This is a LightDM theme for the Webkit greeter which tries to imitate the look and feel of the Mac OSX lion login screen
07.04.2017 - I have forket it and put pull requests to make it look better in my opinion.
Changes were made by https://github.com/mrsim0ns as "Mavericks style background".

Demo:
-------------------------

http://www.youtube.com/watch?v=1Frf3QlZ_gw


Installation Instructions
-------------------------
You will need LightDM as your login manager. On newer versions of Ubuntu and ElementaryOS this is already the default. Additionally you will require the webkit greeter. This is done by executing the following command in the command line:

<pre>
sudo apt-get install lightdm-webkit-greeter
</pre>

Once the installation finishes, you need to make the webkit greeter the default greeter. This is done by editing the lightdm configuration under:
 
<pre>
/etc/lightdm/lightdm.conf
</pre>

and changing the greeter-session value to lightdm-webkit-greeter. My lightdm.conf looks like:

[Seat:*]
greeter-session=lightdm-webkit-greeter
.

The second step is to install the actual theme. This is done by copying the files of this repository into the following location:

<pre>
/usr/share/lightdm-webkit/themes/mac
</pre>

Then change folder permission of images so they can be read with this commands:

<pre>
sudo chmod 744 /usr/share/lightdm-webkit/themes/mac/img
sudo chmod 744 /usr/share/lightdm-webkit/themes/mac/font
</pre>

Finally, change the /etc/lightdm/lightdm-webkit-greeter.conf file to contain the following line: 

<pre>
webkit-theme=mac 
</pre>

Now you can reboot and enjoy the new theme.
