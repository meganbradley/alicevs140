---
title: "CButton::SetNote"
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
ms.assetid: c7c7c31d-8ed9-436d-b23c-fcca516931c4
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetNote
Sets the note text for the current command link control.  
  
## Syntax  
  
```  
BOOL SetNote(  
     LPCTSTR lpszNote  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `lpszNote`|Pointer to a Unicode string that is set as the note text for the command link control.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 Use this method only with controls whose button style is `BS_COMMANDLINK` or `BS_DEFCOMMANDLINK`.  
  
 This method sends the [BCM_SETNOTE](http://msdn.microsoft.com/library/windows/desktop/bb775977) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Example  
 The following code example defines the variable, `m_cmdLink`, that is used to programmatically access the command link control. This variable is used in the following example.  
  
 [!CODE [NVC_MFC_CButton_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton_s1#1)]  
  
## Example  
 The following code example sets the note text for the command link control.  
  
 [!CODE [NVC_MFC_CButton_s1#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton_s1#7)]  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetNote](../vs140/CButton--GetNote.md)   
 [CButton::GetNoteLength](../vs140/CButton--GetNoteLength.md)   
 [BCM_SETNOTE](http://msdn.microsoft.com/library/windows/desktop/bb775977)