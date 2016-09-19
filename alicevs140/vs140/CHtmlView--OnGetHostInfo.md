---
title: "CHtmlView::OnGetHostInfo"
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
ms.assetid: 93753f7a-0f68-472f-9962-c2cedd066171
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnGetHostInfo
Retrieves the UI capabilities of the Internet Explorer or MSHTML host.  
  
## Syntax  
  
```  
  
      virtual HRESULT OnGetHostInfo(  
   DOCHOSTUIINFO *pInfo   
);  
```  
  
#### Parameters  
 `pInfo`  
 Address of a [DOCHOSTUIINFO](https://msdn.microsoft.com/en-us/library/aa770044.aspx) structure that receives the host's UI capabilities.  
  
## Return Value  
 `S_OK` if successful, or an OLE-defined error code otherwise.  
  
## Remarks  
 Override `OnGetHostInfo` to react to the `GetHostInfo` notification from the Microsoft Web Browser control. See [IDocHostUIHandler::GetHostInfo](https://msdn.microsoft.com/en-us/library/aa753257.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::OnGetExternal](../vs140/CHtmlView--OnGetExternal.md)