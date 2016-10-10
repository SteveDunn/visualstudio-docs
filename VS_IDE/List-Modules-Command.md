---
title: "List Modules Command"
ms.custom: na
ms.date: 10/03/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3cb73774-6ac0-43b2-b781-75ed47175bfd
caps.latest.revision: 6
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# List Modules Command
Lists the modules for the current process.  
  
## Syntax  
  
```  
Debug.ListModules [/Address:yes|no] [/Name:yes|no] [/Order:yes|no]  
[/Path:yes|no] [/Process:yes|no] [/SymbolFile:yes|no]  
[/SymbolStatus:yes|no] [/Timestamp:yes|no] [/Version:yes|no]  
```  
  
#### Parameters  
 /Address:`yes|no`  
 Optional. Specifies whether to show the memory addresses of the modules. Default value is `yes`.  
  
 /Name:`yes|no`  
 Optional. Specifies whether to show the names of the modules. Default value is `yes`.  
  
 /Order:`yes|no`  
 Optional. Specifies whether to show the order of the modules. Default value is `no`.  
  
 /Path:`yes|no`  
 Optional. Specifies whether to show the paths of the modules. Default value is `yes`.  
  
 /Process:`yes|no`  
 Optional. Specifies whether to show the processes of the modules. Default value is `no`.  
  
 /SymbolFile:`yes|no`  
 Optional. Specifies whether to show the symbol files of the modules. Default value is `no`.  
  
 /SymbolStatus:`yes|no`  
 Optional. Specifies whether to show the symbol statuses of the modules. Default value is `yes`.  
  
 /Timestamp:`yes|no`  
 Optional. Specifies whether to show the timestamps of the modules. Default value is `no`.  
  
 /Version:`yes|no`  
 Optional. Specifies whether to show the versions of the modules. Default value is `no`.  
  
## Remarks  
  
## Example  
 This example lists the module names, addresses, and timestamps for the current process.  
  
```  
Debug.ListModules /Address:yes /Name:yes /Order:no /Path:no /Process:no /SymbolFile:no /SymbolStatus:no /Timestamp:yes /Version:no  
```  
  
## See Also  
 [Visual Studio Commands](../VS_IDE/Visual-Studio-Commands.md)   
 [Command Window](../VS_IDE/Command-Window.md)   
 [How to: Use the Modules Window](../VS_debugger/How-to--Use-the-Modules-Window.md)