---
title: "Type &#39;&lt;typename&gt;&#39; in assembly &#39;&lt;assemblyname1&gt;&#39; has been forwarded to assembly &#39;&lt;assemblyname2&gt;&#39;"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0f53e613-c1cb-4722-acb5-afa3091e277b
caps.latest.revision: 11
manager: douge
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# Type &#39;&lt;typename&gt;&#39; in assembly &#39;&lt;assemblyname1&gt;&#39; has been forwarded to assembly &#39;&lt;assemblyname2&gt;&#39;
Type '<typename\>' in assembly '<assemblyname1\>' has been forwarded to assembly '<assemblyname2\>'. Either a reference to '<assemblyname2\>' is missing from your project or the type '<typename\>' is missing from assembly '<assemblyname2\>'.  
  
 An expression in the source code for an assembly refers to a type that has been forwarded to another assembly, but the type cannot be found in the destination assembly.  
  
 *Type forwarding* means reassigning the definition of a class, structure, interface, delegate, or enumeration to an assembly other than the one in which it was originally defined. It is often used in conjunction with *code refactoring*, by which you split an assembly into two or more assemblies or move code from one assembly to another.  
  
 Although the type is temporarily still available in the original assembly, it is likely to become undefined when code refactoring removes it from the original assembly.  
  
 **Error ID:** BC31424  
  
### To correct this error  
  
-   Make sure the type is present in the destination assembly.  
  
-   Make sure your project has a reference to the destination assembly.  
  
## See Also  
 <xref:System.Runtime.CompilerServices.TypeForwardedToAttribute?qualifyHint=False>   
 [Type Forwarding (C++/CLI)](../Topic/Type%20Forwarding%20\(C++-CLI\).md)   
 [Managing references in a project](../VS_IDE/Managing-references-in-a-project.md)   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)