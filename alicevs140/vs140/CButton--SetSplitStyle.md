---
title: "CButton::SetSplitStyle"
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
ms.assetid: 95564f4b-af02-448a-b5e2-8f280dde1f6e
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetSplitStyle
Sets the style of the current split button control.  
  
## Syntax  
  
```  
BOOL SetSplitStyle(  
     UINT uSplitStyle  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `uSplitStyle`|A bitwise combination of split button styles. For more information, see the `uSplitStyle` member of the [BUTTON_SPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775955) structure.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 Use this method only with controls whose button style is `BS_SPLITBUTTON` or `BS_DEFSPLITBUTTON`.  
  
 The split button styles specify the alignment, aspect ratio, and graphical format with which Windows draws a split button icon. For more information, see the `uSplitStyle` member of the [BUTTON_SPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775955) structure.  
  
 This method initializes the `mask` member of a [BUTTON_SPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775955) structure with the `BCSIF_STYLE` flag and the `uSplitStyle` member with the `uSplitStyle` parameter, and then sends that structure in the [BCM_GETSPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775969) message that is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_splitButton`, that is used to programmatically access the split button control.  
  
 [!CODE [NVC_MFC_CButton_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton_s1#1)]  
  
## Example  
 The following code example sets the style of the split button drop-down arrow. The `BCSS_ALIGNLEFT` style displays the arrow on the left side of the button, and the `BCSS_STRETCH` style retains the drop-down arrow's proportions when you resize the button.  
  
 [!CODE [NVC_MFC_CButton_s1#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton_s1#3)]  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetSplitStyle](../vs140/CButton--GetSplitStyle.md)   
 [CButton::GetSplitInfo](../vs140/CButton--GetSplitInfo.md)   
 [BCM_SETSPLITINFO](http://msdn.microsoft.com/library/windows/desktop/bb775981)