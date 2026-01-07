# Linux


## Linux File System Overview

1. **/** - Root Folder. Contains everything present on your OS. Similar to C:\ in Windows.

2. **/home** - Contains all of the user data such as the files the user has downloaded and etc.

3. **/etc** - Stores system configuration files like Password rules , Network configs and Installed service settings.

4. **/bin** - Stores all the commands like ls,mv,cat, etc. Works even if system ain't working properly.

5. **/usr** - Stores big software programs and files. Malwares generally hide here and PATH manipulation generally happens here.

6. **/var** - Stores variable data like Logs, Cache, Mails and Spool files.

7. **/tmp** - Stores program related data temporarily. Usually cleared during reboots.

## Navigation Commands conceptual clarity

1. Absolute Path is the complete path location of any file/directory with respect to the root folder. Relative path is the path location of any file/folder with respect to the present working directory.

2. '~' symbol is called tilde and it denotes the '/home/user' directory.

3. Giving just **cd** as input will take you to the User's home directory ('~' directory).

