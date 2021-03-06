###  Autocompletion in federated sharing 

#### Pr: https://github.com/owncloud/ios/pull/606 

Devices:

Server:

Precondition: Set a server with federation app. Set a server as trusted to federated sharing.

---

 
| TestID | Test Case | Steps | Expected Result | Result | Related Comment |
| :-----: | :------- | :---- | :-------------- | :----: | :-------------- |
| 1 | User in other server (with autoc.)|  1. Share a file/folder with a user of a trusted server typing only his name| The autocompletion shows the complete federated URL with format displayName (server)|||
| 2 | User in other server (without autoc.) |  1. Share a file/folder with a user of a non-trusted server typing only his name| When the @ is written is shown as username@ (remote)|||
| 3 | Two users with same name  (with autoc.) |  1. Share a file/folder with a user of a trusted server typing only his name. Another user with the same name exists in the current server| Both users are shown correctly, the remote including whole URL with format displayName (server)|||
| 4 | Two users with same name  (without autoc.) |  1. Share a file/folder with a user of a non-trusted server typing only his name. Another user with the same name exists in the current server| Both users are shown correctly, the remote one including notation "username@ (remote)"|||
| 5 | Three users with same name  (with autoc.) |  1. Share a file/folder with two users of different trusted servers typing only his name. Another user with the same name exists in the current server| Both users are shown correctly, including correct URLs with format displayName (server)|||
| 6 | Three users with same name  (without autoc.) |  1. Share a file/folder with two users of different servers (trusted/non-trusted) typing only his name. Another user with the same name exists in the current server| Both users are shown correctly, including correct URLs with format displayName (server) and the one in non-trusted as username@ (remote)|||
| 7 | Three users end with @ (without autoc.) |  1. Share a file/folder with two users of different servers (trusted/non-trusted) typing only his name that ends with @. Another user with the same name exists in the current server| Both users are shown correctly, including correct URLs  with format displayName (server) and the one in non-trusted as username@ (remote)|||
