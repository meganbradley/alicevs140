---
title: "CPen::GetLogPen"
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
ms.assetid: 9dccf570-0770-4044-86ce-6e39562a90cc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPen::GetLogPen
Gets a `LOGPEN` underlying structure.  
  
## Syntax  
  
```  
  
      int GetLogPen(  
   LOGPEN* pLogPen   
);  
```  
  
#### Parameters  
 `pLogPen`  
 Points to a [LOGPEN](http://msdn.microsoft.com/library/windows/desktop/dd145041) structure to contain information about the pen.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The `LOGPEN` structure defines the style, color, and pattern of a pen.  
  
 For example, call `GetLogPen` to match the particular style of pen.  
  
 See the following topics in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for information about pen attributes:  
  
-   [GetObject](http://msdn.microsoft.com/library/windows/desktop/dd144904)  
  
-   [LOGPEN](http://msdn.microsoft.com/library/windows/desktop/dd145041)  
  
## Example  
 The following code example demonstrates calling `GetLogPen` to retrieve a pen character, and then create a new, solid pen with the same color.  
  
 [!CODE [NVC_MFCDocView#103](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#103)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPen Class](../vs140/CPen-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPen::GetExtLogPen](../vs140/CPen--GetExtLogPen.md)