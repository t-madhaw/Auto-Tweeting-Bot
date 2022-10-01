# Auto-Tweeter Bot

This bot lets you tweet quotes from a .txt file on your computer. You can customise the bot to choose a particular quote from different .txt files within a folder.


### Prerequisites

Before setting up the bot on your local device, you need to:
1. Create a Twitter account,
2. Set up a Twitter Developer account using the same email ID, and
3. Apply for Elevated Access. 

The process of applying for elevated access is rather straightforward and should take no more than 48 hours to be approved once you have applied. Try to be as detailed as possible in your responses. For more instructions, check [this](https://www.jcchouinard.com/apply-for-a-twitter-developer-account/) out.
Once you get approved, you can start setting up the program.

### Installing

1. Go to your Developer's Portal and create an App Environment, generate your tokens. These tokens are unique to your account and sharing them with someone else can be dangerous. 
Once you have generated these tokes, update creds.py.
2. Add the database of tweets you want the bot to post in a .txt file inside the sources folder. Make sure that each tweet is seperated by '$' symbol. (see test1.txt and test2.txt inside sources for reference)
You can add more than one .txt file inside the sources folder.
3. Modify the time interval (line 81) in code.py according to your requirements.
4. Before running the program, ensure that there is an empty folder named tweeted within your root folder.

### Logic of the Program

The program selects a random .txt file from the sources folder. Then it makes a list of quotes(seperated by $) from that .txt file and chooses a random quote from that list. 
It sends the selected quote to be tweeted and removes that quote from that list so it may not be duplicated in future. To keep track of the tweets posted, the quote is added to another .txt file of the same name (a new .txt file is created if it doesn't exist already) in the tweeted folder.

### Future Plans

I am currently learning how to host this bot on AWS Lambda so that it may run even when my system is shut down.


## Authors

* **[t-madhaw](https://github.com/t-madhaw)**  

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details



