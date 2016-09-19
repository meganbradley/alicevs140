---
title: "CHtmlEditCtrlBase::SetShowMiscTags"
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
ms.assetid: 5d7f5abd-b90f-41ea-82f2-6c824e7fe44a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetShowMiscTags
Displays all the tags shown in Microsoft Internet Explorer 4.0.  
  
## Syntax  
  
```  
  
      HRESULT SetShowMiscTags(  
   bool bNewValue   
) const;  
```  
  
#### Parameters  
 `bNewValue`  
 If true, displays all the tags shown in Microsoft Internet Explorer 4.0.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM SHOWMISCTAGS command ID](https://msdn.microsoft.com/en-us/library/aa769952.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetShowMiscTags](../vs140/CHtmlEditCtrlBase--GetShowMiscTags.md)