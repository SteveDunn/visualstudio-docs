---
title: "&#39;AddressOf&#39; expression cannot be converted to &#39;&lt;typename&gt;&#39; because type &#39;&lt;typename&gt;&#39; is declared &#39;MustInherit&#39; and cannot be created"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e8edef15-0df5-46d7-aba6-89e26a2aa506
caps.latest.revision: 10
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
# &#39;AddressOf&#39; expression cannot be converted to &#39;&lt;typename&gt;&#39; because type &#39;&lt;typename&gt;&#39; is declared &#39;MustInherit&#39; and cannot be created
A statement attempts to convert an `AddressOf` expression to a type that can only be a base class and cannot be used to create an instance.  
  
 The `AddressOf` operator creates a procedure delegate instance that references a specific procedure.  
  
 **Error ID:** BC30939  
  
### To correct this error  
  
-   Assign the `AddressOf` expression to a specific delegate type.  
  
## See Also  
 [AddressOf Operator](../Topic/AddressOf%20Operator%20\(Visual%20Basic\).md)   
 [NOT IN BUILD: Delegates and the AddressOf Operator](assetId:///7b2ed932-8598-4355-b2f7-5cedb23ee86f)   
 [Delegates](../Topic/Delegates%20\(Visual%20Basic\).md)