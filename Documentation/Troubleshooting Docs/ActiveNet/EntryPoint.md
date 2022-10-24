If the bi-directional function is not working, you can scan the PDF found in `"\\cvfile01\software\Apps\ActiveNet\EntryPoint\Bi-Directional Scan File.pdf"`
 
Check the EntryPoint UI to ensure the service is reaching the correct station.
 
 ![[ActiveEntryUI 1.png]]
Testing can also be done from here, if this fails check in the ActiveNet Portal under Membership Settings -> EntryPoint -> Workstation Name to find your scan station server name
 
![](C:\Users\schmidtt\OneDrive - City of Vancouver\Documentation\ScreenShots\)
![](C:\Users\schmidtt\OneDrive - City of Vancouver\Documentation\ScreenShots\ActiveNet Server Name.png)
![[ActiveNetServerName2 1.png]]

Ensure this matches the Server_name in the config file, you can find this in `C:\ActiveNetClient\Entrypoint`

![[ActiveNetConfig 1.png]]

We also want to make sure the com port matches the scanner itself in device manager as well as in Activenet.

![[ActiveNetCom.png]]![[ActiveNetCom2.png]]





