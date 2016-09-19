---
title: "CDC::GetTextFace"
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
ms.assetid: e6ef3bc1-361a-4b4a-b89b-e7de0cdc4bfb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetTextFace
Call this member function to copy the typeface name of the current font into a buffer.  
  
## Syntax  
  
```  
  
      int GetTextFace(  
   int nCount,  
   LPTSTR lpszFacename   
) const;  
int GetTextFace(  
   CString& rString   
) const;  
```  
  
#### Parameters  
 `nCount`  
 Specifies the size of the buffer (in bytes). If the typeface name is longer than the number of bytes specified by this parameter, the name is truncated.  
  
 *lpszFacename*  
 Points to the buffer for the typeface name.  
  
 `rString`  
 A reference to a [CString](../vs140/CStringT-Class.md) object.  
  
## Return Value  
 The number of bytes copied to the buffer, not including the terminating null character. It is 0 if an error occurs.  
  
## Remarks  
 The typeface name is copied as a null-terminated string.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetTextMetrics](../vs140/CDC--GetTextMetrics.md)   
 [CDC::SetTextAlign](../vs140/CDC--SetTextAlign.md)   
 [CDC::TextOut](../vs140/CDC--TextOut.md)   
 [GetTextFace](http://msdn.microsoft.com/library/windows/desktop/dd144940)