
>[!INFO]
> Gonna do some tickets
>> Gonna fix some stuff
>> > Continue Doing things
>> > > Go home



* [x] Done
* [ ] Help 
* [x] Test
*
-[x] 

- [ ]


>[!warning]
>this is a warning!

>[!information]

# Heading 1
## Heading 2
### Heading 3

http://obsidian.md - automatic! [Obsidian](http://obsidian.md)


==Highlight me==

```powershell

 NPM(K)    PM(M)      WS(M)     CPU(s)      Id  SI ProcessName
 ------    -----      -----     ------      --  -- -----------
     31    29.99      33.26       0.00    9760   0 ActiveNet.ServiceContainer
     27    24.84      36.55       0.39    2264   1 ApplicationFrameHost
      8     1.66       6.20       0.00    5028   0 armsvc
     15     8.59      19.64       0.19    2768   0 audiodg
     30    30.79       1.68       0.38   18844   1 Calculator
     49    21.29      53.36       0.00   10480   0 CcmExec
      5     2.56       4.61       0.00   14980   0 cmd
     16    23.38      12.04       0.00    5004   0 CmRcService
      7     6.10       5.55       0.00    4800   0 conhost
      7     6.11       7.41       0.00    7020   0 conhost

  
```


```powershell
$Users = (Get-ChildItem -path C:\users).name

                foreach ($User in $Users) {

                     $files = Get-ChildItem C:\users\$user\appdata -Include *.nst, *.ost -Recurse -ea Ignore |  Where LastWriteTime -Lt (Get-Date).AddDays(-60)

  

                     if($null -ne $files){

  

                        Remove-item -Path $files

                     } #
                }
```

==test

**test**

**Bold**

==highlight

```powershell
Test-Connection
```

# header
## header

`inline` 







>[!info]
>When filling up the gas tank ensure the hose nozzle goes _Inside_ the gas tank

>[!warning]
>If the indicator on the fuel gauge is pointing to the letter E the tank *_MUST_* be filled up 🚗 ⛽


**test**
*test*



