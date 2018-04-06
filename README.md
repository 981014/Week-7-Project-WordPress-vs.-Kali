# Project 7 - WordPress Pentesting

Time spent: **8** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Audio Playlist Cross-Site Scripting
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.7.3
  - [X] GIF Walkthrough:
    - [GIF LINK](https://raw.githubusercontent.com/981014/Week-7-Project-WordPress-vs.-Kali/master/XSS%20Playlist.gif)
  - [X] Steps to recreate: 
    - Download the .mp3 from https://www.securify.nl/advisory/SFY20160742/xss.mp3
    - Upload this audio file to Media Library.
    - Create a post with this audio inside a playlist.
  - [X] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/trunk/src/wp-includes/js/mediaelement/wp-playlist.js)
2. (Required) Youtube Embedded Cross-Site Scripting
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.7.3
  - [X] GIF Walkthrough:
    - [GIF LINK](https://raw.githubusercontent.com/981014/Week-7-Project-WordPress-vs.-Kali/master/XSS%20Youtube.gif)
  - [X] Steps to recreate:
    - Create a post with the following text: ```[embed src='http://www.youtube.com/embed/sss\x3csvg onload=alert(1)\x3e'][/embed]```
  - [X] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/trunk/src/wp-includes/embed.php)
3. (Required) Comment Cross-Site Scripting
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [X] GIF Walkthrough:
    - [GIF LINK](https://raw.githubusercontent.com/981014/Week-7-Project-WordPress-vs.-Kali/master/XSS%20Comment.gif)
  - [X] Steps to recreate:
    - Paste the following text in a comment: ```<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>```
    - Make sure the character length is 64kb or more.
  - [X] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/trunk/src/wp-admin/comment.php)
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
