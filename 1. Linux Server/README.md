# Linux Server

It's very hard to try to summarize the Linux skills needed in order to perform at a decent level as a DevOps engineer. That said, there are for sure two topics that are frequently needed:

1. Being able to review and characterize a Linux server. From the (shell) command prompt, you should be able to quickly review a Linux server and find out what's its purpose, how busy it is and if the main applition(s) has obvious errors. See [Quick Linux Server Review](https://docs.sadservers.com/docs/troubleshooting/cant-connect-to-a-service-linux-troubleshooting-guide/#quick-linux-server-review) for example.    
2.  Parsing logs. For instance, given a web server log, finding the number (or rate) of 500 HTTP errors during a unit time.



## 1.1 Objective: Characterize a Linux Server
What’s its purpose, is it busy, does it have errors?

Run the [Linux Server Review](https://sadservers.com/scenario/linux-server-review) scenario to get a Linux server and follow its [Server Review Guide](https://docs.sadservers.com/docs/scenario-guides/practical-linux-server-review/) to achive this objective. 


## 1.2 Objective: Parsing Logs and Metrics
Use commands like: find, grep, cut, uniq, awk, sed, etc to slice and count fields from log files.

Some good exercises are ["The Command Line Murders"](https://sadservers.com/scenario/command-line-murders) , ["Saskatoon": counting IPs](https://sadservers.com/scenario/saskatoon) or ["Lhasa": Easy Math](https://sadservers.com/scenario/lhasa)

