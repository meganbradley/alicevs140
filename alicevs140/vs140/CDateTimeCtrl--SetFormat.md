---
title: "CDateTimeCtrl::SetFormat"
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
ms.assetid: 18035c8e-a246-4e40-9ba5-1a9099bbf0d2
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::SetFormat
Sets the display of a date and time picker control in accordance with a given format string.  
  
## Syntax  
  
```  
  
      BOOL SetFormat(  
   LPCTSTR pstrFormat   
);  
```  
  
#### Parameters  
 *pstrFormat*  
 A pointer to a zero-terminated format string that defines the desired display. Setting this parameter to **NULL** will reset the control to the default format string for the current style.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
> [!NOTE]
>  User input does not determine success or failure for this call.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [DTM_SETFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb761771), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CDateTimeCtrl#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl#6)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)