# uliza-yowsup
Experimenting with yowsup here.

Steps to install:

`sudo apt-get install python-dev`

`sudo pip install yowsup2`

Registration: https://github.com/tgalal/yowsup/wiki/yowsup-cli-2.0#yowsup-cli-registration
then you need to register the phone you plan to work with. Something like this - note check to see which mobile network you are using for the mcc and mnc codes here: https://en.wikipedia.org/wiki/Mobile_country_code and look for Tanzania.  Below is example for airtel

`yowsup-cli registration --requestcode sms --phone 255xxxxxxxxx --cc 255 --mcc 640 --mnc 05`

then you should get an sms code to register - use it like this:

`yowsup-cli registration --register 121-979 --phone 255xxxxxxxxx --cc 255`

You should get a response like this:

status: ok
kind: free
pw: ESYCCDW+/vQM4+FUHpqAc4x6yxx=
price: US$0.99
price_expiration: 1423958598
currency: USD
cost: 0.99
expiration: 1452754091
login: 2557879999xx
type: existing

Finally - create a file in your home directory like /home/user/.config/yowsup/config.txt with this:

 cc=255       #tanzania                                                                                     
 phone=2557879999xx
 id=8685230130259xx      #IMEI found on Android Settings->About phone
 password=ESYCCDW+/vQM4+FUHpqAc4x6yxx= #My whatsapp password followed by one '='~
 
 Finally - you should be able to run it like this: 
 
 `yowsup-cli demos --yowsup --config /home/bart/.config/yowsup/config.txt`
 
 Once started, you can login by typing \L

