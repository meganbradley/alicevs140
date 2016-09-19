---
title: "CBrush::GetLogBrush"
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
ms.assetid: 267220b8-1e7a-4fc8-b49f-b58f7b64312d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBrush::GetLogBrush
Call this member function to retrieve the `LOGBRUSH` structure.  
  
## Syntax  
  
```  
  
      int GetLogBrush(  
   LOGBRUSH* pLogBrush   
);  
```  
  
#### Parameters  
 `pLogBrush`  
 Points to a [LOGBRUSH](http://msdn.microsoft.com/library/windows/desktop/dd145035) structure that contains information about the brush.  
  
## Return Value  
 If the function succeeds, and `pLogBrush` is a valid pointer, the return value is the number of bytes stored into the buffer.  
  
 If the function succeeds, and `pLogBrush` is **NULL**, the return value is the number of bytes required to hold the information the function would store into the buffer.  
  
 If the function fails, the return value is 0.  
  
## Remarks  
 The `LOGBRUSH` structure defines the style, color, and pattern of a brush.  
  
 For example, call `GetLogBrush` to match the particular color or pattern of a bitmap.  
  
## Example  
 [!CODE [NVC_MFCDocView#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#27)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CBrush Class](../vs140/CBrush-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LOGBRUSH](http://msdn.microsoft.com/library/windows/desktop/dd145035)   
 [GetObject](http://msdn.microsoft.com/library/windows/desktop/dd144904)