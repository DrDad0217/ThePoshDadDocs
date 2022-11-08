
```powershell
$SiloPCs = @('VPD523724L', 'VPD522971D', 'VPD523121L', 'VPD502943D', 'VPD523017L', 'VPD522718D', 'VPD523123L', 'VPD522216D', 'VPD523725L', 'VFD811690L')

$Computers = Ping-test $SiloPCs | Where status -eq 'online'

  
  $Machines = foreach ($computer in $Computers.Computername) {

  

    $Session = New-PSSession -ComputerName $Computer

  

    Start-COVsoftwaresearch -ComputerName $computer | Where displayname -Like 'authentic8'

  

    #Copy-item -Path 'C:\users\schmidtt\Downloads\authentic8-win-2.9.19-17-g4cbad16-release-prod.msi' -ToSession $Session -Destination 'C:\Support\Downloads'

  

    Remove-PSSession -Session $Session

  

}

  

foreach ($Machine in $Machines.PSComputerName) {

  

    Invoke-command -computername $Machine -ScriptBlock { Start-Process "C:\Support\Downloads\authentic8-win-2.9.19-17-g4cbad16-release-prod.msi" }

}

```