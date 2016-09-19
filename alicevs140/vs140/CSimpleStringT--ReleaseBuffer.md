---
title: "CSimpleStringT::ReleaseBuffer"
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
ms.assetid: ff0a3476-a7c4-4dc4-89fc-713fcfcdab16
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::ReleaseBuffer
Releases control of the buffer allocated by [GetBuffer](../vs140/CSimpleStringT--GetBuffer.md).  
  
## Syntax  
  
```  
  
      void ReleaseBuffer(  
   int nNewLength = -1  
);  
```  
  
#### Parameters  
 `nNewLength`  
 The new length of the string in characters, not counting a null terminator. If the string is null terminated, the -1 default value sets the `CSimpleStringT` size to the current length of the string.  
  
## Remarks  
 Call this method to reallocate or free up the buffer of the string object. If you know that the string in the buffer is null terminated, you can omit the `nNewLength` argument. If your string is not null terminated, use `nNewLength` to specify its length. The address returned by [GetBuffer](../vs140/CSimpleStringT--GetBuffer.md) is invalid after the call to `ReleaseBuffer` or any other `CSimpleStringT` operation.  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::ReleaseBuffer`.  
  
 [!CODE [NVC_ATLMFC_Utilities#87](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#87)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)