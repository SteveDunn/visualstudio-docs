---
title: "IDiaAddressMap::get_imageAlign"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f1ba8071-669c-4cf7-9ac0-02f26d99f366
caps.latest.revision: 8
manager: ghogen
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
# IDiaAddressMap::get_imageAlign
Retrieves the current image alignment.  
  
## Syntax  
  
```cpp#  
HRESULT get_imageAlign (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns  the image alignment value from the executable.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Images are aligned to specific memory boundaries depending how the image was loaded and created. The alignment is typically on 1, 2, 4, 8, 16, 32, or 64 byte boundaries. The image alignment can be set with a call to the [IDiaAddressMap::put_imageAlign](../VS_debugger/IDiaAddressMap--put_imageAlign.md) method.  
  
## See Also  
 [IDiaAddressMap](../VS_debugger/IDiaAddressMap.md)   
 [IDiaAddressMap::put_imageAlign](../VS_debugger/IDiaAddressMap--put_imageAlign.md)