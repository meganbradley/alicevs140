---
title: "CToolBarCtrl::SetColorScheme"
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
ms.assetid: 53e3b954-4d00-4d12-86da-298608e0b298
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetColorScheme
Sets the color scheme of the current toolbar control.  
  
## Syntax  
  
```  
void SetColorScheme(  
     const COLORSCHEME* lpColorScheme  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `lpColorScheme`|Pointer to a [COLORSCHEME](http://msdn.microsoft.com/library/windows/desktop/bb775502) structure that describes the highlight color and shadow color of the toolbar control.|  
  
## Remarks  
 This method has no effect if a [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] visual theme is set.  
  
 This method sends the [TB_SETCOLORSCHEME](http://msdn.microsoft.com/library/windows/desktop/bb787421) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Example  
 The following code example sets the color scheme for the current toolbar control. The code example makes the left and top edges of each tool button red and the right and bottom edges blue. When the user presses the button, the button's red edges turn blue and its blue edges turn red.  
  
 [!CODE [NVC_MFC_CToolBarCtrl_s1#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CToolbarCtrl_s1#3)]  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TB_SETCOLORSCHEME](http://msdn.microsoft.com/library/windows/desktop/bb787421)   
 [COLORSCHEME](http://msdn.microsoft.com/library/windows/desktop/bb775502)   
 [CToolBarCtrl::GetColorScheme](../vs140/CToolBarCtrl--GetColorScheme.md)