Project 7 - WordPress Pentesting

Time spent: 5 hours spent in total

Objective: Find, analyze, recreate, and document 3 vulnerabilities affecting an old version of WordPress

Pentesting Report:
1. WordPress => 4.2 - Authenticated Stored Cross-Site Scripting (XSS)
 Summary:
Vulnerability types: XSS,
Tested in version: <= 4.2.3,
Fixed in version: 4.2,
 
GIF Walkthrough:
![vulnerability xss](https://user-images.githubusercontent.com/42792775/47959227-b34bd980-dfb4-11e8-9a74-9c105750565e.gif)
Steps to recreate:
Make a new post
Write the javascript "<SCRIPT>alert('XSS')</SCRIPT>" in lower case.
Publish it, then view the post.

2. WordPress =>4.2 - Authenticated Stored Cross-Site Scripting (XSS) via Image frame Summary
 Summary:
Vulnerability types: XSS,
Tested in version: 4.2.1,
Fixed in version: 4.2,
GIF Walkthrough: 

![vulnerability2 xss](https://user-images.githubusercontent.com/42792775/47959240-06259100-dfb5-11e8-8131-09b369f8e930.gif)

Steps to recreate:
 Add a new image in library. 
 Then go to library and click on that image. 
 In the title section, add the javascript "<img src= a onerror=alert(1)>.png" right next to the image name.

3. WordPress => 4.2 - User Authentication
 Summary:
Vulnerability types: user authentication,
Fixed in version: 4.2,
 GIF Walkthrough: 
 
 ![vulnerability3](https://user-images.githubusercontent.com/42792775/47959247-3d943d80-dfb5-11e8-9957-ed055526c7e8.gif)


Steps to recreate:
Enter "admin" as username and type random password.
Enter "different name" as username and type "admin" as password.

Assets

List any additional assets, such as scripts or files

Resources

WordPress Source Browser
WordPress Developer Reference
GIFs created with LiceCap.

Notes

Took some time to figure out how to appraoch.

License

Copyright [2018] [Mahmudul Hasan]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
 




 
