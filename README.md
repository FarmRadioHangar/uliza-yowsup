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

`status: ok
kind: free
pw: ESYCCDW+/vQM4+FUHpqAc4x6y1A=
price: US$0.99
price_expiration: 1423958598
currency: USD
cost: 0.99
expiration: 1452754091
login: 255787999994
type: existing
`


