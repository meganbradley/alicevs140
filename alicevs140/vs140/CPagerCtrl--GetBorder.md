---
title: "CPagerCtrl::GetBorder"
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
ms.assetid: 60e1e989-4bc5-4687-80d2-53c0758d8ff3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::GetBorder
Retrieves the border size of the current pager control.  
  
## Syntax  
  
```  
int GetBorder() const;  
```  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Return Value  
 The current border size, measured in pixels.  
  
## Remarks  
 This method sends the [PGM_GETBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760869) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 The following example uses the [CPagerCtrl::GetBorder](../vs140/CPagerCtrl--GetBorder.md) method to retrieve the thickness of the pager control's border.  
  
 [!CODE [NVC_MFC_CSplitButton_s2#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CSplitButton_s2#5)]  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PGM_GETBORDER](http://msdn.microsoft.com/library/windows/desktop/bb760869)   
 [CPagerCtrl::SetBorder](../vs140/CPagerCtrl--SetBorder.md)