#Articles

[Powershell: Installing MSI files (powershellexplained.com)](https://powershellexplained.com/2016-10-21-powershell-installing-msi-files/)

$DataStamp = get-date -Format yyyyMMddTHHmmss

$logFile = '{0}-{1}.log' -f $Using:file.fullname,$DataStamp

$MSIArguments = @(

    "/i"

    ('"{0}"' -f $file.fullname)

    "/qn"

    "/norestart"

    "/L*v"

    $logFile

)

Start-Process "msiexec.exe" -ArgumentList $MSIArguments -Wait -NoNewWindow

  

$File = Get-item 'C:\Support\Downloads\vlc-3.0.17.4-win64.exe'

  

$Session = New-PSSession -ComputerName VPD523019L

  

Copy-Item -Path '\\cvfile01\Software\Apps\codecs\VLC\vlc-3.0.17.4-win64.exe' -ToSession $Session -Destination 'C:\Support\Downloads'

  

Invoke-Command -Session $Session -ScriptBlock {

$file = Get-item 'C:\Support\Downloads\vlc-3.0.17.4-win64.exe'

$DataStamp = get-date -Format yyyyMMddTHHmmss

$logFile = '{0}-{1}.log' -f $file.fullname,$DataStamp

$MSIArguments = @(

    "/i"

    ('"{0}"' -f $file.fullname)

    "/qn"

    "/norestart"

    "/L*v"

    $logFile

)

  

Start-Process "msiexec.exe" -ArgumentList $MSIArguments -Wait -NoNewWindow

}

