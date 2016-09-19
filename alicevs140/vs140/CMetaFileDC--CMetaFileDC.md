---
title: "CMetaFileDC::CMetaFileDC"
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
ms.topic: reference
ms.assetid: fa5879ac-e6ee-4522-8b09-6d92f50eee26
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMetaFileDC::CMetaFileDC
Construct a `CMetaFileDC` object in two steps.  
  
## Syntax  
  
```  
  
CMetaFileDC( );  
```  
  
## Remarks  
 First, call `CMetaFileDC`, then call **Create**, which creates the Windows metafile device context and attaches it to the `CMetaFileDC` object.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CMetaFileDC Class](../vs140/CMetaFileDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMetaFileDC::Create](../vs140/CMetaFileDC--Create.md)