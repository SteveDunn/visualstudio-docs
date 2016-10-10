---
title: "Compiler Error CS1922"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a4098a25-6581-4966-b61d-318cd12f76d3
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
# Compiler Error CS1922
Collection initializer requires its type 'type' to implement System.Collections.IEnumerable.  
  
 In order to use a collection initializer with a type, the type must implement `IEnumerable`. This error can occur if you accidentally use collection initializer syntax when you meant to use an object initializer.  
  
### To correct this error  
  
-   If the type does not represent a collection, use object initializer syntax instead of collection initializer syntax.  
  
-   If the type does represent a collection, modify it to implement `IEnumerable` before you can use collection initializers to initialize objects of that type.  
  
-   If the type represents a collection and you do not have access to the source code, just initialize its elements by using their class constructors or other initialization methods.  
  
## Example  
 The following code produces CS1922:  
  
```  
// cs1922.cs  
public class Test  
{  
    public static void Main()  
    {  
        // Collection initializer.  
        var tc = new TestClass  {1,"hello"} ; // CS1922  
  
        // Object initalizer.  
        var tc2 = new TestClass { memberA = 1, memberB = "hello" }; // OK  
    }  
}  
  
public class TestClass  
{  
    public int memberA { get; set; }  
    public string memberB { get; set; }  
}  
  
```  
  
## See Also  
 [Object and Collection Initializers](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md)