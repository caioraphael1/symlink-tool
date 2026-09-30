
# Symlink Tool

- Parses `.link` files that define how symlinks should be created for both files and directories.
- Created to automate symlink creation while documenting path relationships, making it incredibly useful for maintaining a fully declarative file system.


## Usage

- `.link` file: 
```txt
// Alacritty
<symlink destination> <symlink origin>
```

- Executable:
```sh
.\symlink_tool.exe <link file (.link)> <source directory>
```


### Example

- Uses the configurations defined in `file.link`, with `C:\caio\apps` as the base directory for resolving the symlink destination specified in the `.link` file.

- `file.link`: 
```txt
// Alacritty
"%USERPROFILE%\AppData\Roaming\alacritty" "alacritty\config"
```
- Executing:
```sh
.\symlink_tool.exe "C:\caio\programming\symlink_tool\files\file.link" "C:\caio\apps"
```


## Build

- Cannot be built, as it uses the Dusk programming language, which is not yet available.
- Once available, the app is built by:
```sh
dusk build .
```


## TODO

- [ ] Check pathing for the source; currently the Source Dir is not being used, and I'm not sure it should.
- [ ] Support for hardlink. Test hardlink for KeePassXC by just using the terminal; if it works, cool.
