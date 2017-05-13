[![Version](https://img.shields.io/badge/Meterpreter_Paranoid_Mode-1.2-brightgreen.svg?maxAge=259200)]()
[![Stage](https://img.shields.io/badge/Release-Alpha-brightgreen.svg)]()
[![Build](https://img.shields.io/badge/Supported_OS-kali,Ubuntu,Mint,Parrot-blue.svg)]()


![Meterpreter_Paranoid_Mode v1.2](http://2.1m.yt/fgzGtKJ.png)


## Meterpreter_Paranoid_Mode v1.2 - SSL/TLS connections
    Version release: v1.2 (Alpha)
    Author: pedro ubuntu [ r00t-3xp10it ]
    Distros Supported : Linux Ubuntu, Kali, Mint, Parrot OS
    Suspicious-Shell-Activity (SSA) RedTeam develop @2017

<br /><br />

## Description:
     Meterpreter_Paranoid_Mode.sh allows users to secure your staged/stageless
     connection for Meterpreter by having it check the certificate of the
     handler it is connecting to.

     We start by generating a certificate in PEM format, once the certs have
     been created we can create a HTTP or HTTPS or EXE payload for it and give
     it the path of PEM format certificate to be used to validate the connection.
     To have the connection validated we need to tell the payload what certificate
     the handler will be using by setting the path to the PEM certificate in the
     HANDLERSSLCERT option then we enable the checking of this certificate by
     setting stagerverifysslcert to true.

     Once that payload is created we need to create a handler to receive the
     connection and again we use the PEM certificate so the handler can use the
     SHA1 hash for validation. Just like with the Payload we set the parameters
     HANDLERSSLCERT with the path to the PEM file and stagerverifysslcert to true. 


    When we get payload execution, we can see the stage doing the validation
![Meterpreter_Paranoid_Mode v1.2](http://3.1m.yt/Gsm4ejx.png)

 
## Exploitation:
    Meterpreter_Paranoid_Mode tool starts posgresql service, builds the PEM certificate,
    builds payload (staged OR stageless), and starts the corespondent handler associated
    to the PEM certificate created (manual) OR impersonated (msf auxliary module) ..
![Meterpreter_Paranoid_Mode v1.2](http://3.1m.yt/quzn56A.png)

<br /><br />

## Dependencies/Limitations:
    xterm, zenity, metasploit, postgresql

<br /><br />

## Download/Install/Config:
    1º - Download framework from github
         git clone https://github.com/r00t-3xp10it/Meterpreter_Paranoid_Mode-SSL.git

    2º - Set files execution permitions
         cd Meterpreter_Paranoid_Mode-SSL
         sudo chmod +x *.sh

    4º - Run main tool
         sudo ./Meterpreter_Paranoid_Mode.sh

<br /><br />

## Tool screenshots
![Meterpreter_Paranoid_Mode v1.2](http://4.1m.yt/6SrdKEM.png)
![Meterpreter_Paranoid_Mode v1.2](http://1.1m.yt/em7t0J6.png)
![Meterpreter_Paranoid_Mode v1.2](http://2.1m.yt/ws0tkJU.png)
![Meterpreter_Paranoid_Mode v1.2](http://2.1m.yt/5dgO89S.png)
![Meterpreter_Paranoid_Mode v1.2](http://3.1m.yt/F31lEJV.png)

<br />

## Video tutorials:
FakeImageExploiter [ Official release - Main funtions ]: https://www.youtube.com/watch?v=4dEYIO-xBHU

FakeImageExploiter [ the noob friendly funtion ]: https://www.youtube.com/watch?v=abhIp-SG4kM

<br />

### Special thanks:
**@hdmoore** | **@OJ** | **@darkoperator**

Credits:
http://buffered.io/posts/staged-vs-stageless-handlers/

https://github.com/rapid7/metasploit-framework/wiki/Meterpreter-Paranoid-Mode

https://www.darkoperator.com/blog/2015/6/14/tip-meterpreter-ssl-certificate-validation

**Suspicious-Shell-Activity (SSA) RedTeam develop @2017**
