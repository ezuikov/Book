# New-Rendering

Creates new rendering definition that can later be added to an item.

## Syntax

New-Rendering \[-Item\] &lt;Item&gt; \[-Parameter &lt;Hashtable&gt;\] \[-PlaceHolder &lt;String&gt;\] \[-DataSource &lt;Item&gt;\] \[-Cacheable\] \[-VaryByData\] \[-VaryByDevice\] \[-VaryByLogin\] \[-VaryByParameters\] \[-VaryByQueryString\] \[-VaryByUser\] \[-Language &lt;String\[\]&gt;\]

New-Rendering \[-Path\] &lt;String&gt; \[-Parameter &lt;Hashtable&gt;\] \[-PlaceHolder &lt;String&gt;\] \[-DataSource &lt;Item&gt;\] \[-Cacheable\] \[-VaryByData\] \[-VaryByDevice\] \[-VaryByLogin\] \[-VaryByParameters\] \[-VaryByQueryString\] \[-VaryByUser\] \[-Language &lt;String\[\]&gt;\]

New-Rendering -Id &lt;String&gt; \[-Database &lt;String&gt;\] \[-Parameter &lt;Hashtable&gt;\] \[-PlaceHolder &lt;String&gt;\] \[-DataSource &lt;Item&gt;\] \[-Cacheable\] \[-VaryByData\] \[-VaryByDevice\] \[-VaryByLogin\] \[-VaryByParameters\] \[-VaryByQueryString\] \[-VaryByUser\] \[-Language &lt;String\[\]&gt;\]

## Detailed Description

Creates new rendering definition that can later be added to an item. Most parameters can later be overriden when calling Add-Rendering.

© 2010-2017 Adam Najmanowicz, Michael West. All rights reserved. Sitecore PowerShell Extensions

## Parameters

### -Parameter  &lt;Hashtable&gt;

Rendering parameters as hashtable

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -PlaceHolder  &lt;String&gt;

Placeholder for the rendering to be placed into.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -DataSource  &lt;Item&gt;

Datasource for the rendering.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -Cacheable  &lt;SwitchParameter&gt;

Defined whether the rendering is cacheable.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -VaryByData  &lt;SwitchParameter&gt;

Defines whether a data-specific cache version of the rendering should be kept.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -VaryByDevice  &lt;SwitchParameter&gt;

Defines whether a device-specific cache version of the rendering should be kept.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -VaryByLogin  &lt;SwitchParameter&gt;

Defines whether a login - specific cache version of the rendering should be kept.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -VaryByParameters  &lt;SwitchParameter&gt;

Defines whether paremeter - specific cache version of the rendering should be kept.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -VaryByQueryString  &lt;SwitchParameter&gt;

Defines whether query string - specific cache version of the rendering should be kept.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -VaryByUser  &lt;SwitchParameter&gt;

Defines whether a user - specific cache version of the rendering should be kept.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -Language  &lt;String\[\]&gt;

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -Item  &lt;Item&gt;

The item to be processed.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | true |
| Position? | 1 |
| Default Value |  |
| Accept Pipeline Input? | true \(ByValue, ByPropertyName\) |
| Accept Wildcard Characters? | false |

### -Path  &lt;String&gt;

Path to the item to be processed - can work with Language parameter to narrow the publication scope.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | true |
| Position? | 1 |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -Id  &lt;String&gt;

Id of the item to be processed - can work with Language parameter to narrow the publication scope.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | true |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

### -Database  &lt;String&gt;

Database containing the item to be processed - can work with Language parameter to narrow the publication scope.

| Aliases |  |
| --- | --- | --- | --- | --- | --- |
| Required? | false |
| Position? | named |
| Default Value |  |
| Accept Pipeline Input? | false |
| Accept Wildcard Characters? | false |

## Inputs

The input type is the type of the objects that you can pipe to the cmdlet.

* Sitecore.Data.Items.Item 

## Outputs

The output type is the type of the objects that the cmdlet emits.

* Sitecore.Layouts.RenderingDefinitio 

## Notes

Help Author: Adam Najmanowicz, Michael West

## Examples

### EXAMPLE

find item defining rendering and create rendering definitio

```text
PS master:\> $renderingItem = gi master:\layout\Sublayouts\ZenGarden\Basic\Content | New-Rendering -Placeholder "main"
# find item you want the rendering added to
PS master:\> $item = gi master:\content\Demo\Int\Home
# Add the rendering to the item
PS master:\> Add-Rendering -Item $item -PlaceHolder "main" -Rendering $renderingItem -Parameter @{ FieldName = "Content" }
```

## Related Topics

* [https://github.com/SitecorePowerShell/Console/](https://github.com/SitecorePowerShell/Console/) 
* [Add-Rendering](add-rendering.md)
* [Set-Rendering](set-rendering.md)
* [Get-Rendering](get-rendering.md)
* [Get-LayoutDevice](get-layoutdevice.md)
* [Remove-Rendering](remove-rendering.md)
* [Get-Layout](get-layout.md)
* [Set-Layout](set-layout.md)

