---
title: "CBookmark::CBookmark"
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
ms.assetid: 84f4ad2b-67d4-4ba3-8b2b-656a66fb6298
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBookmark::CBookmark
The constructor.  
  
## Syntax  
  
```  
  
      CBookmark( );   
CBookmark(  
   DBLENGTH nSize   
);  
```  
  
#### Parameters  
 `nSize`  
 [in] Size of the bookmark buffer in bytes.  
  
## Remarks  
 The first function sets the buffer to **NULL** and the buffer size to 0. The second function sets the buffer size to `nSize`, and the buffer to a byte array of `nSize` bytes.  
  
> [!NOTE]
>  This function is only available in **CBookmark<0>**.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CBookmark Class](../vs140/CBookmark-Class.md)