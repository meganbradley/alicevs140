---
title: "CFont::CFont"
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
ms.assetid: a8f47b1f-d579-4991-82a8-513da631ed02
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFont::CFont
Constructs a `CFont` object.  
  
## Syntax  
  
```  
  
CFont( );  
```  
  
## Remarks  
 The resulting object must be initialized with `CreateFont`, `CreateFontIndirect`, `CreatePointFont`, or `CreatePointFontIndirect` before it can be used.  
  
## Example  
 [!CODE [NVC_MFCDocView#70](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#70)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFont Class](../vs140/CFont-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFont::CreateFontIndirect](../vs140/CFont--CreateFontIndirect.md)   
 [CFont::CreateFont](../vs140/CFont--CreateFont.md)   
 [CFont::CreatePointFont](../vs140/CFont--CreatePointFont.md)   
 [CFont::CreatePointFontIndirect](../vs140/CFont--CreatePointFontIndirect.md)   
 [EnumFonts](http://msdn.microsoft.com/library/windows/desktop/dd162622)