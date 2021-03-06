# Interfaces

Here we'll discuss the Console, ISE, and other dialogs made available through SPE.

![The Sitecore PowerShell Console is a command line interface that many power users find great for quickly running commands.](../.gitbook/assets/cli-empty.png)

![The Sitecore PowerShell ISE is a scripting interface for running commands and authoring scripts.](../.gitbook/assets/ise-empty.png)

## Providers

You can interact with the providers typically available in the standard Windows PowerShell Console. Below are some of the important providers. Run the command `Get-PSProvider` to see the complete list.

* **FileSystem** - Supports interacting with files and folders.
* **CmsItemProvider** - Supports interacting with the Sitecore content items.

The console prompt typically begins with `PS master:\>`. The present working directory is using the _CmsItemProvider_ and set to the _master_ database.

**Example:** Change directories between providers.

```text
 PS master:\> cd core:
 PS core:\> cd C:
 PS C:\windows\system32\inetsrv> Set-Location -Path master:
 PS master:\>
```

**Note:** Include the backslash in the path \(i.e. **C:\**\) to get the root of the drive when interacting with the _FileSystem_ provider; the behavior seen is different than you might expeect because of _w3wp.exe_. See issue \#[314](https://github.com/SitecorePowerShell/Console/issues/314).

## Variables

Read more about the different variables [here](variables.md).

