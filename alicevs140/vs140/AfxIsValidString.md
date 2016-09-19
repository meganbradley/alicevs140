---
title: "AfxIsValidString"
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
ms.assetid: 11c8b14f-0b1a-4717-882c-843efbdbf4ac
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxIsValidString
Use this function to determine whether a pointer to a string is valid.  
  
## Syntax  
  
```  
  
      BOOL AfxIsValidString(  
   LPCSTR lpsz,  
   int nLength = -1   
);   
```  
  
#### Parameters  
 `lpsz`  
 The pointer to test.  
  
 `nLength`  
 Specifies the length of the string to be tested, in bytes. A value of –1 indicates that the string will be null-terminated.  
  
## Return Value  
 In debug builds, nonzero if the specified pointer points to a string of the specified size; otherwise 0.  
  
 In non-debug builds, nonzero if `lpsz` is not NULL; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#29)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxIsMemoryBlock](../vs140/AfxIsMemoryBlock.md)   
 [AfxIsValidAddress](../vs140/AfxIsValidAddress.md)