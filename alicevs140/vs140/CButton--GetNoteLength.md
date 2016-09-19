---
title: "CButton::GetNoteLength"
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
ms.assetid: a324b9b4-164b-4023-8478-144e5fc85442
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::GetNoteLength
Retrieves the length of the note text for the current command link control.  
  
## Syntax  
  
```  
UINT GetNoteLength() const;  
```  
  
## Return Value  
 The length of the note text, in 16-bit Unicode characters, for the current command link control.  
  
## Remarks  
 Use this method only with controls whose button style is `BS_COMMANDLINK` or `BS_DEFCOMMANDLINK`.  
  
 This method sends the [BCM_GETNOTELENGTH](http://msdn.microsoft.com/library/windows/desktop/bb775967) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::GetNote](../vs140/CButton--GetNote.md)   
 [CButton::SetNote](../vs140/CButton--SetNote.md)   
 [BCM_GETNOTELENGTH](http://msdn.microsoft.com/library/windows/desktop/bb775967)