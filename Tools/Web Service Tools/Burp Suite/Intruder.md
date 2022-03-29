- Arguably the most powerful tool in Burp Suite. Intruder can be used for many things from fuzzing to brute-forcing but at the end of the day intruder serves one purpose: automation!
- Once you know a vulnerability exists it's time to use Intruder to rip it apart. It's common uses are
	- Enumerating identifiers such as usernames, cycling through predictable session/password recovery tokens and attempting simple password guessing
	- Harvesting useful data from user profiles or other pages of interest via grepping our responses
	- Fuzzing for vulnerabilities such as SQL injection, cross-site scripting, and file path traversal.
- Intruder has four different attack types which are as follows
## Sniper
- Sniper is the most popular attack type and for a good reason. Sniper cycles through selected positions, putting the next available payload in each position in turn. All you have to do is feed it a single wordlist and aim.
## Battering Ram
- Like Sniper battering ram only uses one wordlist but instead of cycling through each selected position Battering Ram puts each string from the wordlist in each position. 
## Pitchfork
- Pitchfork is useful when you need multiple payload sets for different forms. This is most commonly used when you have a username form and a username wordlist + a password form and a password wordlist. Pitchfork will only go as far as the smallest payload set provided so if you have a 10 line wordlist and a 10,000,000 line wordlist Pitchfork will go 10 times.
## Cluster Bomb
- Cluster bomb is the ultimate throwing everything at the wall type of strategy. It works similar to Pitchfork except for one thing, it will cycle through every possible option. With Pitchfork you could have a 10 line wordlist and a 10,000,000 line wordlist and only have it go 10 times, cluster bomb would go 100,000,000 times. This can take a while.