---
title: "Compiler Error CS0516"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0516"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0516"
ms.assetid: a9de9d1d-9ee3-4533-ba31-b8cb9f9964a1
caps.latest.revision: 6
ms.author: "billchi"
manager: "douge"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Compiler Error CS0516
Constructor 'constructor' can not call itself  
  
 A program cannot recursively call constructors.  
  
 The following sample generates CS0516:  
  
```  
// CS0516.cs  
namespace x  
{  
   public class clx  
   {  
      public clx() : this()   // CS0516, delete "this()"  
      {  
      }  
  
      public static void Main()  
      {  
      }  
   }  
}  
```