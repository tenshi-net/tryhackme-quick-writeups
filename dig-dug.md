# Dig Dug

[This challenge room](https://tryhackme.com/room/digdug) is **remarkably** simple. The tool you use is right in the room's name: you'll use the `dig` command to figure out the answer. Starting off, I did a simple `dig` command to get the DNS record type: `dig givemetheflag.com`

The output of that command tells you that the givemetheflag.com domain is an A record, the standard DNS address record type. 

From there, finding the answer is just one command away. This time, you'd run `dig @[TARGET_IP] givemetheflag.com A`. This will give you a full output on the domain's DNS info, including the flag which shows up under the section labeled `;; ANSWER SECTION:`.
