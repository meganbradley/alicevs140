---
title: "CDateTimeCtrl::GetRange"
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
ms.assetid: afc48ec4-334d-4ede-b56f-39be0e28a0a9
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::GetRange
Retrieves the current minimum and maximum allowed system times for a date and time picker control.  
  
## Syntax  
  
```  
  
      DWORD GetRange(  
   COleDateTime* pMinRange,  
   COleDateTime* pMaxRange   
) const;  
DWORD GetRange(  
   CTime* pMinRange,  
   CTime* pMaxRange   
) const;  
```  
  
#### Parameters  
 `pMinRange`  
 A pointer to a [COleDateTime](../vs140/COleDateTime-Class.md) object or a [CTime](../Topic/CTime%20Class.md) object containing the earliest time allowed in the `CDateTimeCtrl` object.  
  
 `pMaxRange`  
 A pointer to a `COleDateTime` object or a `CTime` object containing the latest time allowed in the `CDateTimeCtrl` object.  
  
## Return Value  
 A `DWORD` value containing flags that indicate which ranges are set. If  
  
 `return value & GDTR_MAX` == 0  
  
 then the second parameter is valid. Similarly, if  
  
 `return value & GDTR_MIN` == 0  
  
 then the first parameter is valid.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [DTM_GETRANGE](http://msdn.microsoft.com/library/windows/desktop/bb761767), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. In MFC's implementation, you can specify either `COleDateTime` or `CTime` usages.  
  
## Example  
 [!CODE [NVC_MFC_CDateTimeCtrl#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl#4)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDateTimeCtrl::SetRange](../vs140/CDateTimeCtrl--SetRange.md)