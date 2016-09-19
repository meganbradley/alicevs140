---
title: "CPen::CreatePenIndirect"
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
ms.assetid: e86ee5d5-25aa-4521-9570-180efe92bb8d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPen::CreatePenIndirect
Initializes a pen that has the style, width, and color given in the structure pointed to by `lpLogPen`.  
  
## Syntax  
  
```  
  
      BOOL CreatePenIndirect(  
   LPLOGPEN lpLogPen   
);  
```  
  
#### Parameters  
 `lpLogPen`  
 Points to the Windows [LOGPEN](../vs140/LOGPEN-Structure.md) structure that contains information about the pen.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 Pens that have a width greater than 1 pixel should always have either the **PS_NULL**, **PS_SOLID**, or **PS_INSIDEFRAME** style.  
  
 If a pen has the **PS_INSIDEFRAME** style and a color that does not match a color in the logical color table, the pen is drawn with a dithered color. The **PS_INSIDEFRAME** style is identical to **PS_SOLID** if the pen width is less than or equal to 1.  
  
## Example  
 [!CODE [NVC_MFCDocView#101](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#101)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPen Class](../vs140/CPen-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPen::CreatePen](../vs140/CPen--CreatePen.md)   
 [CPen::CPen](../vs140/CPen--CPen.md)