
This case shows inconsistent exit codes of PowerShell.exe when it is invoked
with seemingly same commands.

If the command `'Hello, world!'; Write-Error Oops` is invoked by PowerShell.exe
then its exit code is 1. But if it is placed in a script and the script is
invoked then the exit code is 0.

Scripts

- *Script.with.command.ps1* contains the command.
- *Test-Script.with.command.ps1* invokes 3 tests:
    - invokes the command directly
    - invokes it as the script
    - dot-sources the script
