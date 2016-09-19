---
title: "IDiaAddressMap::put_imageAlign"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f9ce875d-c263-43e5-a534-f34c37f9866f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaAddressMap::put_imageAlign
Sets the image alignment.  
  
## Syntax  
  
```cpp#  
HRESULT put_imageAlign (   
   DWORD NewVal  
);  
```  
  
#### Parameters  
 NewVal  
 [in] The new image alignment value for the executable.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Images (loaded executables) are aligned to specified memory boundaries. This alignment can be affected by the current system architecture and by compile and link time options. Image alignment is always on byte boundaries. The following image alignment values are valid: 1, 2, 4, 8, 16, 32, and 64 byte boundaries.  
  
 The current image alignment can be retrieved with a call to the [IDiaAddressMap::get_imageAlign](../vs140/IDiaAddressMap--get_imageAlign.md) method.  
  
> [!NOTE]
>  The image is already loaded by the time this method can be called. The `put_imageAlign` method is typically used when the image has been moved or changed and a new alignment is required.  
  
## See Also  
 [IDiaAddressMap](../vs140/IDiaAddressMap.md)   
 [IDiaAddressMap::get_imageAlign](../vs140/IDiaAddressMap--get_imageAlign.md)