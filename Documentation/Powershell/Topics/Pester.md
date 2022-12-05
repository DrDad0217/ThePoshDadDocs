```powershell
Describe 'Start-CovSoftwareSearch' {

  

    BeforeAll{

  

        . $PSScriptRoot/Start-COVSoftwareSearch.ps1

    }

  

    It 'Accepts pipeline input ByPropertyName' {

        $ComputerName = 'INT012055T'

        $Search = $ComputerName | Start-COVSoftwareSearch

        $Search.Count | Should -BeGreaterThan 0

  
  

    }

  

    It 'Accepts pipeline input ByValue' {

  

      $Search =  'INT012055T' | Start-COVSoftwareSearch

      $Search.Count | Should -BeGreaterThan 0

  
  

    }
```