# Create Desktop shortcuts with Microsoft Intune

Create and remediate desktop (and start menu) shortcuts with Microsoft Intune using Win32 apps. This solution works with OneDrive Known Folder Move. Because the Desktop is not stored in the default user profile location.

Usage: ```CreateDesktopIcon.exe -ShortcutTargetPath "\\app01.intra.contoso.com\Programme\abacus.abalink" -ShortcutDisplayName "Abacus"```

The "Add-Shortcut.ps1" script is wrapped in an exe with the [PS2EXE-GUI](https://gallery.technet.microsoft.com/scriptcenter/PS2EXE-GUI-Convert-e7cb69d5). Which one is again wrapped as Intune Win32 app with the [Win32 Content Prep Tool](https://github.com/Microsoft/Microsoft-Win32-Content-Prep-Tool).

The desktop location is determined with the variable: ```[Environment]::GetFolderPath("Desktop")```