---
title: "CEdit::GetHighlight"
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
ms.assetid: 86badba0-60f6-4ad8-a2c9-49057962c1fe
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::GetHighlight
Gets the indexes of the first and last characters in a range of text that is highlighted in the current edit control.  
  
## Syntax  
  
```  
BOOL GetHighlight(  
     int* pichStart,   
     int* pichEnd  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `pichStart`|Zero-based index of the first character in the range of text that is highlighted.|  
|[out] `pichEnd`|Zero-based index of the last character in the range of text that is highlighted.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [EM_GETHILITE](http://msdn.microsoft.com/library/windows/desktop/bb761578) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::SetHighlight](../vs140/CEdit--SetHighlight.md)   
 [EM_GETHILITE](http://msdn.microsoft.com/library/windows/desktop/bb761578)