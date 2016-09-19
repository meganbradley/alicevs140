---
title: "CStrBufT::SET_LENGTH"
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
ms.assetid: 37ac08ea-2992-4a0a-acbd-dfe672107852
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStrBufT::SET_LENGTH
Set the length of the string object at `GetBuffer` time.  
  
## Syntax  
  
```  
  
static const DWORD SET_LENGTH = 0x02;  
  
```  
  
## Remarks  
 Set the length of the string object at GetBuffer time.  
  
 Determines if [CSimpleStringT::GetBuffer](../vs140/CSimpleStringT--GetBuffer.md) and [CSimpleStringT::GetBufferSetLength](../vs140/CSimpleStringT--GetBufferSetLength.md) are called when the string buffer object is constructed.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStrBufT Class](../vs140/CStrBufT-Class.md)   
 [CStrBufT::CStrBufT](../vs140/CStrBufT--CStrBufT.md)