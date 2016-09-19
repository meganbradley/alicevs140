---
title: "CBookmark::SetBookmark"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bcd26831-6045-4e69-96d6-abf8037fc18d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBookmark::SetBookmark
Copies the bookmark value referenced by `pBuffer` to the `CBookmark` buffer and sets the buffer size to `nSize`.  
  
## Syntax  
  
```  
  
      HRESULT SetBookmark(  
   DBLENGTH nSize,  
   BYTE* pBuffer   
) throw( );  
```  
  
#### Parameters  
 *nSize*  
 [in] The size of the bookmark buffer.  
  
 `pBuffer`  
 [in] A pointer to the byte array containing the bookmark value.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 This function is only available in **CBookmark<0>**.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CBookmark Class](../vs140/CBookmark-Class.md)