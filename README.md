

# KNSHelper

Provide some generic helpers functions for Powershell.

## ConvertTo-Slug
### Synopsis
Slugify a String in entry
### Syntax
```powershell
ConvertTo-Slug [-Text] <String> [[-Delimiter] <String>] [-CapitalizeFirstLetter] [<CommonParameters>]
```
### Parameters
| Name  | Alias  | Description | Required? | Pipeline Input | Default Value |
| - | - | - | - | - | - |
| <nobr>Text</nobr> |  | String. Text to slugify | true | true \(ByValue\) |  |
| <nobr>Delimiter</nobr> |  | String. Optional, the delimiter used. If omitted, "-" will be used | false | false | - |
| <nobr>CapitalizeFirstLetter</nobr> |  | Switch. If the switch is set, it will capitalize the first letter of each word in the "Text" string. | false | false | False |
### Examples

**EXAMPLE 1**
```powershell
ConvertTo-Slug "That's all folks!"
```
Will return "thats-all-folks"

**EXAMPLE 2**
```powershell
ConvertTo-Slug "That's all Folks!" -Delimiter "_"
```
Will return "thats\_all\_folks"

**EXAMPLE 3**
```powershell
ConvertTo-Slug "That's all Folks!" -Delimiter "" -CapitalizeFirstLetter
```
Will return "ThatsAllFolks"

