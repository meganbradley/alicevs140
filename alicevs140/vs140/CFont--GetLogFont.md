---
title: "CFont::GetLogFont"
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
ms.assetid: 277832a9-82f3-4257-9b75-ddda68577ba6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFont::GetLogFont
Call this function to retrieve a copy of the `LOGFONT` structure for `CFont`.  
  
## Syntax  
  
```  
  
      int GetLogFont(  
   LOGFONT * pLogFont   
);  
```  
  
#### Parameters  
 *pLogFont*  
 Pointer to the [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/dd145037) structure to receive the font information.  
  
## Return Value  
 Nonzero if the function succeeds, otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCDocView#76](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#76)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFont Class](../vs140/CFont-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LOGFONT](http://msdn.microsoft.com/library/windows/desktop/dd145037)   
 [GetObject](http://msdn.microsoft.com/library/windows/desktop/dd144904)