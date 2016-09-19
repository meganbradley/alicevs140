---
title: "CDC::BeginPath"
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
ms.assetid: db3ab7ec-345f-4a9c-a494-627ce8e36fbd
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::BeginPath
Opens a path bracket in the device context.  
  
## Syntax  
  
```  
BOOL BeginPath();  
```  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 After a path bracket is open, an application can begin calling GDI drawing functions to define the points that lie in the path. An application can close an open path bracket by calling the `EndPath` member function. When an application calls `BeginPath`, any previous paths are discarded.  
  
 See [BeginPath](http://msdn.microsoft.com/library/windows/desktop/dd183363) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a list of the drawing functions that define points in a path.  
  
## Example  
 [!CODE [NVC_MFCDocView#30](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#30)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::EndPath](../vs140/CDC--EndPath.md)   
 [CDC::FillPath](../vs140/CDC--FillPath.md)   
 [CRgn::CreateFromPath](../vs140/CRgn--CreateFromPath.md)   
 [CDC::SelectClipPath](../vs140/CDC--SelectClipPath.md)   
 [CDC::StrokeAndFillPath](../vs140/CDC--StrokeAndFillPath.md)   
 [CDC::StrokePath](../vs140/CDC--StrokePath.md)   
 [CDC::WidenPath](../vs140/CDC--WidenPath.md)