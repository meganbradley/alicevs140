---
title: "CBasePane::get_accHelpTopic"
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
ms.assetid: 46c5d590-9c32-42e5-b687-f98008172848
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::get_accHelpTopic
The framework calls this method to retrieve the full path of the `WinHelp` file that is associated with the specified object and the identifier of the appropriate topic in that file.  
  
## Syntax  
  
```  
virtual HRESULT get_accHelpTopic(  
   BSTR *pszHelpFile,  
   VARIANT varChild,  
   long *pidTopic  
);  
```  
  
#### Parameters  
 [in] `pszHelpFile`  
 Address of a `BSTR` that receives the full path of the `WinHelp` file that is associated with the specified object, if any.  
  
 [in] `varChild`  
 Specifies whether the Help topic to be retrieved is that of the object or one of the child elements of the object. This parameter can be either `CHILDID_SELF` (to obtain a Help topic for the object) or a child ID (to obtain a Help topic for one of the child elements of the object).  
  
 [in] `pidTopic`  
 Identifies the `Help` file topic that is associated with the specified object.  
  
## Return Value  
 `CBasePane` does not implement this method. Therefore, `CBasePane::get_accHelpTopic` always returns `S_FALSE`.  
  
## Remarks  
 This function is part of the Active Accessibility support in MFC. Override this function in a derived class to provide help information about your object.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)