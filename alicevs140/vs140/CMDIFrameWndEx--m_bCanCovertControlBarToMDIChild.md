---
title: "CMDIFrameWndEx::m_bCanCovertControlBarToMDIChild"
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
ms.assetid: d78d757e-47e8-4eb7-a61e-24be379403bc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::m_bCanCovertControlBarToMDIChild
Specifies whether docking panes can be converted to MDI child windows.  
  
## Syntax  
  
```  
BOOL m_bCanCovertControlBarToMDIChild;  
```  
  
## Remarks  
 Indicates whether docking control bars can be converted to MDI child windows. If this flag is `TRUE`, the framework handles the conversion automatically when the user selects the **Tabbed Document** command. The flag is protected and you must explicitly enable this option either by setting `m_bCanCovertControlBarToMDIChild` in a constructor of a `CMDIFrameWndEx`-derived class, or by overriding `CanConvertControlBarToMDIChild`.  
  
 The default value is `FALSE`.  
  
## Example  
 The following example shows how `m_bCanCovertControlBarToMDIChild` is used in the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#13](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#13)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)