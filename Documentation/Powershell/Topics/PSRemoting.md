- Enable-PSRemoting gives the client the ability for incoming Powershell commands
- Enable-PSRemoting only creates an endpoint for the current version of powershell you are running the command in


#### Enable-PSRemoting runs the `Set-WSManQuickConfig` cmdlet which runs the following tasks

-   Starts the WinRM service.
-   Sets the startup type on the WinRM service to Automatic.
-   Creates a listener to accept requests on any IP address.
-   Enables a firewall exception for WS-Management communications.
-   Creates the simple and long name session endpoint configurations if needed.
-   Enables all session configurations.
-   Changes the security descriptor of all session configurations to allow remote access.