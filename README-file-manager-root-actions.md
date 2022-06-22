## Filemanager root actions
To get the root actions on Manjaro install the package zensu and create files as follows

## Open Folder as Root

> `~/.local/share/file-manager/actions/openasroot.desktop`

```
[Desktop Entry]
Type=Action
Name=Open Folder as Root
Icon=dialog-password
Profiles=profile-openfolderasroot

[X-Action-Profile profile-openfolderasroot]
MimeTypes=inode/directory;
Exec=zensu pcmanfm %u
Name=Default profile
```

## Edit as Root

> `~/.local/share/file-manager/actions/editasroot.desktop`

```
[Desktop Entry]
Type=Action
Name=Edit as Root
Name[fr]=Editer en tant que root
Name[de]=Bearbeiten als root
Icon=dialog-password
Profiles=profile-editasroot;profile-editasroot2;

[X-Action-Profile profile-editasroot]
MimeTypes=text/*;
TryExec=leafpad
Exec=zensu leafpad %f
Name=Default profile

[X-Action-Profile profile-editasroot2]
MimeTypes=application/x-desktop;
Exec=zensu leafpad %f
Name=Default profile
```
