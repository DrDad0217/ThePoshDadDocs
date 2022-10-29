```powershell
$Object = [PSCustomObject]@{

            BaseProperty = 17

        }
```

Current output 
```
BaseProperty
------------
          17
```

Adding a  member named ==Derived Value== and referencing the `Object.Baseproperty` with the `$this`
automatic variable. 



```powershell
$Object | Add-Member -MemberType ScriptProperty -Name DerivedProperty -Value {

            # ScriptProperties can reference their parent object using $this

            $this.BaseProperty++

            $this.BaseProperty % 4

        }
```

#### Adding script properties with custom getters and setters

```powershell
 $Object = [PSCustomObject]@{

            BaseProperty = 11

        }
```

```powershell

$Object.PSObject.Properties.Add(

            # A script property can consist of a name, a getter, and (optionally) a setter.

            [psscriptproperty]::new('CustomProperty',

                {

                    # getter

                    $this.BaseProperty + 1

                },

                {

                    # setter

                    param($val)

                    $this.BaseProperty = - [int]($val)

                }

            )

        )
```
