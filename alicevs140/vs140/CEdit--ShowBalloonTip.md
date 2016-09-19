---
title: "CEdit::ShowBalloonTip"
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
ms.assetid: 8b3cbae5-b7c0-48d0-b244-9215b73a6fc3
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::ShowBalloonTip
Displays a balloon tip that is associated with the current edit control.  
  
## Syntax  
  
```  
BOOL ShowBalloonTip(  
     PEDITBALLOONTIP pEditBalloonTip  
);  
BOOL ShowBalloonTip(  
     LPCWSTR lpszTitle,   
     LPCWSTR lpszText,   
     INT ttiIcon = TTI_NONE  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `pEditBalloonTip`|Pointer to an [EDITBALLOONTIP](http://msdn.microsoft.com/library/windows/desktop/bb775466) structure that describes the balloon tip.|  
|[in] `lpszTitle`|Pointer to a Unicode string that contains the title of the balloon tip.|  
|[in] `lpszText`|Pointer to a Unicode string that contains the balloon tip text.|  
|[in] `ttiIcon`|An `INT` that specifies the type of icon to associate with the balloon tip. The default value is `TTI_NONE`. For more information, see the `ttiIcon` member of the [EDITBALLOONTIP](http://msdn.microsoft.com/library/windows/desktop/bb775466) structure.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This function sends the [EM_SHOWBALLOONTIP](http://msdn.microsoft.com/library/windows/desktop/bb761668) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For more information, see the [Edit_ShowBalloonTip](http://msdn.microsoft.com/library/windows/desktop/bb761707) macro.  
  
## Example  
 The following code example defines a variable, `m_cedit`, that is used to access the current edit control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CEdit_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit_s1#1)]  
  
## Example  
 The following code example displays a balloon tip for an edit control. The [CEdit::ShowBalloonTip](../vs140/CEdit--ShowBalloonTip.md) method specifies a title and balloon tip text.  
  
 [!CODE [NVC_MFC_CEdit_s1#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit_s1#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
 This control is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::HideBalloonTip](../vs140/CEdit--HideBalloonTip.md)   
 [EM_SHOWBALLOONTIP](http://msdn.microsoft.com/library/windows/desktop/bb761668)   
 [EDITBALLOONTIP](http://msdn.microsoft.com/library/windows/desktop/bb775466)   
 [Edit_ShowBalloonTip](http://msdn.microsoft.com/library/windows/desktop/bb761707)