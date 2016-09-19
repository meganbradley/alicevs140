---
title: "CHtmlEditCtrlBase::GetShowMiscTags"
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
ms.assetid: e898d3d3-82cb-4263-b31b-47968133d610
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetShowMiscTags
Retrieves whether the WebBrowser displays all the tags shown in Microsoft Internet Explorer 4.0.  
  
## Syntax  
  
```  
  
      HRESULT GetShowMiscTags(  
   bool& bCurValue   
) const;  
```  
  
#### Parameters  
 `bCurValue`  
 True if the WebBrowser displays all the tags shown in Microsoft Internet Explorer 4.0, false if it does not.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 For more information, see [IDM_SHOWMISCTAGS Command ID](https://msdn.microsoft.com/en-us/library/aa769952.aspx).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetShowMiscTags](../vs140/CHtmlEditCtrlBase--SetShowMiscTags.md)