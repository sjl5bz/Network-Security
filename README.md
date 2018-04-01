# Network-Security
Network Security
# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Authenticated Shortcode Tags Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.5
  - [ ] GIF Walkthrough: ![xss2](https://user-images.githubusercontent.com/15334096/38174230-31899160-3598-11e8-8228-2aa46e740ec9.gif)
  - [ ] Steps to recreate: Create a post or page. Click on text instead of visual and insert a caption with the XSS attack. I used an alert. ``` TEST!!![caption width="1" caption='<a href="' ">]<a href="http://onMouseOver='alert(2)'">Click me</a>```
  - [ ] Affected source code: <img width="498" alt="screen shot 2018-04-01 at 10 15 10 am" src="https://user-images.githubusercontent.com/15334096/38174105-5cef7ae2-3596-11e8-8a7f-0dcd5815c6f4.png">
    - [Link 1](http://blog.knownsec.com/2015/09/wordpress-vulnerability-analysis-cve-2015-5714-cve-2015-5715/)
2. (Required) Unauthenticated Stored XSS
  - [ ] Summary: Created a cross site scripting attack using a window alert
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: ![xss](https://user-images.githubusercontent.com/15334096/38169106-dac0eaae-352e-11e8-9e42-2c37fdc20bd1.gif)
  - [ ] Steps to recreate: Post a reply on one of the pages. Insert javascript for alert: ``` <a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>```  and make sure message is bigger than 64kb. Then when submitted, an alert box should appear.
  - [ ] Affected source code: 

    - [Link 1](http://klikki.fi/adv/wordpress2.html)
3. (Required) Authenticated Cross-Site Scripting (XSS) via Media File Metadata
  - [ ] Summary: XSS vulnerability when uploading audio files. Attacker can upload malicious mp3 files which can be executed when you create an audio playlist. Meta information in audio files are not properly sanitized. 
    - Vulnerability types: XSS
    - Tested in version: 4.2 
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: ![xss3](https://user-images.githubusercontent.com/15334096/38174776-a192d0d6-35a0-11e8-8912-0ebdfcf7b48d.gif)
  - [ ] Steps to recreate: Upload the malicious mp3 file into media. Then create an audio playlist with the malicious file. Insert the audio playlist into a post/page. 
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7)
4. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
5. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
