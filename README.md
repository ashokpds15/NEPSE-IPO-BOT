IPO Bot
This is selenium based bot made in Python to automate the IPO application process

Getting up and running ( Installation )
Check out the repository from Github

git clone git@github.com:bistasulove/ipo-bot.git
cd ipo-bot
Install Python (if not already)

Note: This project is running Python 3.9.10.

Create Virtual Envrinoment Note: This step is optional but it is highly recommended you create a virtual environment so that you don't mess up dependencies.

Create Virtual Environment On MacOS or Linux

python -m venv myvenv
Note: You might need to use python3 instead of python based on your python installation.

Create Virtual Environment On Windows

python -m venv myvenv
Activate Virtual Environment on MacOS or Linux

source myvenv/bin/activate
Activate Virtual Environment on Windows

myvenv\Scripts\activate
Install Dependencies

Use pip to install all the dependencies listed in requirements.txt file

pip install -r requirements.txt
Service Configuration

You are supposed to create a .env file if you want to harness the feature of the bot:

Create a .env file inside the project root directory (ipo-bot)
Following environment variables are being used currently:
RECURRING_CUSTOMER - if value is set to True (RECURRING_CUSTOMER='True'), it checks the saved config from env file. Otherwise, it will ask the user input for which share to apply.
APPLY_ORDINARY_SHARES - if set to True (APPLY_ORDINARY_SHARES='True'), it will apply only Ordinary Shares and not Debentures
APPLY_ALL - if set to True (APPLY_ALL='True'), it will apply all of the shares
APPLY_FIRST - if set to True (APPLY_FIRST='True'), it will apply only the first share in the Open issues page
Demat configuration

You are supposed to add the details of yours and others demat accounts in user_details.csv file.

Sample user_details.csv file

alias	dp_id	username	password	crn	txn_pin	apply_unit
LOVE  10100 12345678  09876543  vab112  1111  10
FOREVER 11200 213456  00973898  45678912  2222  20
Running program

 python main.py
Note: This project assumes that you have Google Chrome installed. Please change the driver in driver.py if you want to run other browser.
