[Work With Me](../resume_page.md), [Projects](../projects.md), [Blog](../blog.md)

# MOTD and other Fun Configs
So few people spend the time to setup their computers to really reflect them that it's a bit of a shame. And it's especially a shame among IT type people who are supposed to treat their computers with a bit more enjoyment. There are a few enjoyable things that I've setup on a decent (but not all) number of the servers that I operate on regularly. 

## MOTD
First thing, set your MOTD. Message of the Day (MOTD) is the item that gets displayed when you first connect to a machine via SSH. This can be either a file, where i like to set some [ASCII Art](https://www.asciiart.eu/). Or even better, you can write a little script to give you a constantly updating motd with relevant information. When I was last using cloud init on some Ubuntu images I set the motd to cowsay the hostname. Not normally super useful, but in this particular setup it was useful because these servers were being created and destroyed with such regularity that the IP addresses were not always what we thought they were and it made a good quick sanity check. Message of the day is a great way to differentiate different servers, or proivde immediately relevant information upon connection. 

One possible use of the MOTD which has occured to me is to get a LLM utility to summarize the current messages at the systme level and provide a summary of any issues whcih may have occured in the past X length of time. 
## Cowsay
When it's avialable, let a cow say it. cowsay is such a simple little package, but it adds some needed joy to terminal. Piping stuff in and out of cowsay can make the part that you're actually doing a bit more interesting. Piping cowsay into wall for sending shutdown messages is a great way to actually grab someones attention on the terminal. adding figlet and toilet into the mix can make for some nice banners, creating ascii / text banners of whatever is input. Although I have yet to figure out a reliable way to pipe any of these formatted outputs into cowsay reliably. It would be very nice to be able to pipe fancy text like this into cowsay to get fancy cowsay outputs. 

## Neofetch
Neofetch. Although it's apparently discontinued, I'm sure that someone, or many someones will pick it up shortly enough. I wasn't a huge fan; however, a lot of people apparently adore tweaking their neofetch to make it look as pretty as possible. I can even install it via windows package manager winget and produce my windows decide specifications. 

## SSH Keys
Add your SSH keys to your github and use them for all your logins. We all know that public keys are and should be publicly available. That's kind of their point. Making all your servers no longer accept password authentication for remote SSH is generally good practice. But to set your auth keys you can add your keys first to your github account and then use that to make downloading them to everywehre easier. [My Public Keys](https://github.com/devinatkin.keys). It's a useful enough fact that Ubuntu even includes github as a easy import source for authorized keys during the operating system install. 

### Reverse SSH Tunnel
Creating a Reverse SSH Tunnel, although I always need to double check the syntax.

```bash
ssh -R [local_port]:localhost:[remote_port] [user]@[remote_host]
```

This creates a reverse SSH tunnel and allows the local port to be accesssible on the remote machine. I've used this to be able to get out of peoples home networks when needing to access their machines remotely. A point to keep in mind and avoid breaking is that the connection will due, and you'll need to keep it alive by either keeping it active, or by re-establishing it whenever it fails. 

```bash
ssh -f -N -o ServerAliveInterval=60 -o ServerAliveCountMax=3 -R [local_port]:localhost:[remote_port] [user]@[remote_host]
```
This keeps the server connection alive by sending messages at 60 second intervals. It also moves SSH into the background while not executing anything on the remote machine. Even this will eventually die when the person has a network failure or something similar, so it's important to couple this with some form of code set to just re-establish the connection if it has failed. 

## Smaller Tools

### htop
A nicer version of top. Great for monitoring a system as it runs a bunch of processes you want to keep an eye on. The cleaner human readable interface makes for a much easier time when things are changing. Plus everyone loves colourful terminals. 

### jq
A simple json hanlder perfect for command line usage. Great for extracting specific information without needing to dig deeply into the overarching structure of the code. 

### fzf
A simple utility to allow for simple selection without being fancy and writing out the full utilities. Simply use the barebones user interface to select the actual value that you want. 

### ncdu
NCurses Disk Usage tool. It looks over all your files and provides a simple user interface for seeing where all that storage is actually going. 

### asciinema
Instead of recording a screen recording of your terminal and wasting all that extra space, record the actual text as you type it and the timing there-in. Simple enough to use, and can be either streamed or cast to elsewhere as needed. 