Got that new machine smell? Run this:

    if (-not ([Security.Principal.WindowsPrincipal][Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] "Administrator")) { throw "You need to run this from an elevated PS prompt" }; Set-ExecutionPolicy RemoteSigned -Force; iex ((new-object net.webclient).DownloadString('https://raw.githubusercontent.com/dimitar/New-Machine.ps1/master/New-Machine.ps1'))

You trust me, right?
