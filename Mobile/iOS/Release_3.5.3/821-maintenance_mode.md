###  Maintenance mode 

#### Pr: https://github.com/owncloud/ios/pull/821 

Devices: iPhone6 Plus v 10.1.1, iPad Air v9.3.3

Server: 9.1.3


---

 
| TestID | Test Case | Steps | Expected Result | Result | Related Comment |
| :----: | :-------- | :---- | :-------------- | :----: | :-------------- |
|**Operations**|||||||
| 1 | Login | With maintenance mode enabled, login in the app | Not possible. Message is shown | P m10 t9 |  |
| 2 | Download file| With maintenance mode enabled, download a file | Not possible. Message is shown | P m10 t9|  |
| 3 | Download folder| With maintenance mode enabled, download a folder | Not possible. Message is shown | P m10 t9|  |
| 4 | Upload file| With maintenance mode enabled, upload a file | Not possible. Message is shown. File is not queued | P m10 t9|  |
| 5 | Instant Upload | 1. With maintenance mode enabled, take a photo with instant uploads enabled<br> 2. Disable maintenance mode| 1. Photo is queued, but not uploaded.<br>2. Photo is uploaded | P m10 t9|  |
| 6 | Share with external app | With maintenance mode enabled, share a file  | 1. Photo is queued, but not uploaded.<br>2. Photo is uploaded | P m10 t9|  |
| 7 | New folder | With maintenance mode enabled, create a new folders | Not possible. Message is shown | P m10 t9|  |
| 8 | Rename | With maintenance mode enabled, rename a file | Not possible. Message is shown | P m10 t9|  |
| 9 | Move | With maintenance mode enabled, move a file | Not possible. Message is shown | P m10 t9|  |
| 10 | Txt file | With maintenance mode enabled, create a txt file | File is queued but not uploaded (queued) | P m10 t9|  |
| 11 | Remove | With maintenance mode enabled, remove a file | Not possible. Message is shown | P m10 t9|  |
| 12 | Share with users/groups | With maintenance mode enabled, share with a user/group | Not possible. Message is shown | P m10 t9|  |
| 13 | Share by link | With maintenance mode enabled, share by link | Not possible. Message is shown | P m10 t9|  |
| 14 | Av offline | With maintenance mode enabled, set a file as av. offline | File is set but content is not downloaded. Message is shown | P m10 t9| SOLVED: Files and folders behave different |
|**Multiaccount**|||||||
| 15 | Both in maintenance | Set several accounts, all of them in maintenance mode. Try several options | Message is always shown | P t9 m10|  |
| 16 | Some in maintenance | Set several accounts, some of them in maintenance mode. Try several options in all account | Message is shown if it is in maintenance, not shown if not in maintenance | P t9 m10|  |
|**Special servers**|||||||
| 17 | Redirected server | Set a redirected server in maintenance mode. Try several options | Message is always shown | P m10 t9 |  |
| 18 | Shibboleth server | Set a shibboleth server in maintenance mode. Try several options | Message is always shown | P m10 t9 | SOLVED: Maintenance mode not notified |
