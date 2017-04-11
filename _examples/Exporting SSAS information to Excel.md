---
title: Exporting information from SSAS
layout: example
---

If you want to get information out of powerSSAS into Excel you can use the Export-Csv cmdlet that is built-in to PowerShell. Something like the following would export a 
list of dimensions to a .csv file. 

```powershell
add-PSSnapin powerssas
new-PSDrive ssas powerssas localhost
cd ssas:
cd "Databases\Adventure Works DW\Dimensions"

# this lists out all the properties
dir | export-Csv c:\dims.csv
```

 And if you only wanted certain properties, you could change the last line to something like the following, using the select-object cmdlet (aliased as "select" in this example) to only return the specified properties: 

```powershell
dir | Select Name,State,LastSchemaUpdate,LastProcessed | export-Csv c:\dims2.csv
```

If you really have special requirements, or if you simply need to use a delimiter other than a comma (eg. if your region uses commas for the decimal separator) then you could roll your own string and redirect that to a file. 

```powershell
add-PSSnapin powerssas
new-PSDrive ssas powerssas localhost
cd ssas:
cd "Databases\Adventure Works DW\Dimensions"
# loop through the dimensions and 
# redirect the constructed string to a file
$( 
  foreach ($d in get-ChildItem)
  {
    "$($d.Name)`t$($d.State)"
  } 
) > c:\dims.txt
```

Note that Powershell uses the backtick (`) as an escape character, so the `t is interpreted as a tab character and I am collecting the whole loop up inside an expression $(...) and redirecting that through to a file. 

Finally if you wanted absolute control over the output, you could instantiate a copy of Excel and control it using the COM object model. 

```powershell
$objXL = New-Object -comobject Excel.Application
```

But there are issues with that approach, not the least of which is the fact that it does not work on my laptop! Trying to call the Add method of the Workbooks collection throws the following unhelpful error: 

```
"Exception calling "add" with "0" arguement(s): 
"Old format or invalid type library. 
<Exception from HRESULT: 0x80028018 <Type_E_INVDATAREAD>>"_
```

This is possibly because I am using a regional setting of en-AU, not en-US. As googling for this issue turned up the following KB article which was useful - [http://support.microsoft.com/kb/320369](http://support.microsoft.com/kb/320369). 

Using the suggested InvokeMember work around looked promising and I did manage to get Excel working to a degree, but I am not going to bother posting that code here as it was pretty messy. And I could not get the second suggested work around of changing the culture of the current thread to work at all from PowerShell.