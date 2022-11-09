# Stock-News

Stock News App

Automated self messaging app to never miss the most important news on the stock market price of the company of your desire.

This application is installable locally in desktop.

## Built With

- Python

## Getting Started

To get a local copy up and running follow these simple example steps.

### Setup

- Open the console
- Download or git clone https://github.com/AllanAscencio/stock-news
- cd stock-news
- Create your account on https://newsapi.org/ in order to get your free API, to see their documentation here https://newsapi.org/docs
- Create your account on https://www.twilio.com/ in order to get your free API and AUTH, to see their documentation visit https://www.twilio.com/docs/sms
- To get the stock market data you need to register https://www.alphavantage.co/support/#api-key to get your API Key and documentation here https://www.alphavantage.co/documentation/

Install requests:

Linux

```
  $ pip install requests 
```

In Linux, If you require root permission, use ‘sudo’. Alternatively, you can also use pipenv to install requests library, where pipenv is used to automatically manage the packages during the course of installation/uninstallation.

```
$ pip install pipenv
```

Windows

The Windows users need to navigate to the Python directory, and then install the request module as follows:

```
> python -m pip install requests
```

Mac
For MacOS, install Python through ‘Home Brew’. Thereafter, install pip and request module (which is the same as Linux installation process.)

Install twilio:

The easiest way to install the library is from PyPi using pip, a package manager for Python. Simply run this in a terminal:

```
pip3 install twilio
```
If you get a pip: command not found error, you can also use easy_install. Run this in your terminal:

```
easy_install twilio
```
Manual twilio installation

Alternatively, you can download the source code (ZIP) for twilio-python https://github.com/twilio/twilio-python/zipball/main, and then install the library by running: 
```
python3 setup.py install
```
in the folder containing the twilio-python library.

“Permission Denied”
If the command line gives you a big long error message that says Permission Denied in the middle of it, try running the above commands with sudo (e.g., sudo pip3 install twilio).

### Test your installation

Try sending yourself an SMS message. Save the following code sample to your computer with a text editor. Be sure to update the account_sid, auth_token, and from_ phone number with values from your Twilio account. The to phone number can be your own mobile phone.
```
from twilio.rest import Client

# Your Account SID from twilio.com/console
account_sid = "ACXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
# Your Auth Token from twilio.com/console
auth_token  = "your_auth_token"

client = Client(account_sid, auth_token)

message = client.messages.create(
    to="+15558675309", 
    from_="+15017250604",
    body="Hello from Python!")

print(message.sid)
```

Author
👤 **Allan Ascencio**

- [Github](https://github.com/AllanAscencio)
- [Linkedin]((https://www.linkedin.com/in/gianfranco-allan))


## Considerations

- Since this webpages are constantly updating structures on their JSON data you might want to check with a JSON viewer the dictionaries to use the correct ones specially on https://www.alphavantage.co/ and https://newsapi.org/
- You can always update the code to get more than the top 3 news and edit the slice up to how many you want about the stock price of a certain company, which in this code Tesla is set as the default company

## 🤝 Contributing

Contributions, issues and feature requests are welcome!

## Show your support

Give a ⭐️ if you like this project!

## 📝 License

This project is [MIT](https://opensource.org/licenses/MIT) licensed.
