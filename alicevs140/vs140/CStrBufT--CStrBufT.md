---
title: "CStrBufT::CStrBufT"
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
ms.assetid: 34d71f8e-e38c-453e-9e3e-c97346ef00ff
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStrBufT::CStrBufT
Constructs a buffer object.  
  
## Syntax  
  
```  
  
      CStrBufT(  
   StringType& str,  
   int nMinLength,  
   DWORD dwFlags = AUTO_LENGTH   
) throw(...);  
explicit CStrBufT(  
   StringType& str   
) throw(...);  
```  
  
#### Parameters  
 `str`  
 The string object associated with the buffer. Typically, the developer will use the predefined typedefs of **CStrBuf** (**TCHAR** variant), **CStrBufA** (`char` variant) and **CStrBufW** (`wchar_t` variant).  
  
 *nMinLength*  
 The minimum length of the character buffer.  
  
 `dwFlags`  
 Determines if the string length is automatically determined. Can be one of the following:  
  
-   **AUTO_LENGTH** String length is automatically determined when [CSimpleStringT::Release](../vs140/CSimpleStringT--ReleaseBuffer.md) is called. The string must be null-terminated. Default value.  
  
-   **SET_LENGTH** String length is set when [CSimpleStringT::GetBuffer](../vs140/CSimpleStringT--GetBuffer.md) is called.  
  
## Remarks  
 Creates a string buffer for the associated string object. During construction, [CSimpleStringT::GetBuffer](../vs140/CSimpleStringT--GetBuffer.md) or [CSimpleStringT::GetBufferSetLength](../vs140/CSimpleStringT--GetBufferSetLength.md) is called.  
  
 Note that the copy constructor is `private`.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStrBufT Class](../vs140/CStrBufT-Class.md)   
 [CStrBufT::StringType](../vs140/CStrBufT--StringType.md)