---
title: "CHtmlView::OnGetOptionKeyPath"
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
ms.assetid: dd104a93-d3bf-45e6-affd-34edcd112729
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnGetOptionKeyPath
Call this member function to get the registry key under which Internet Explorer or MSHTML stores user preferences.  
  
## Syntax  
  
```  
  
      virtual HRESULT OnGetOptionKeyPath(  
   LPOLESTR* pchKey,  
   DWORD dwReserved   
);  
```  
  
#### Parameters  
 `pchKey`  
 Address of an `LPOLESTR` that receives the registry subkey string where the host stores its default options. This subkey will be under the HKEY_CURRENT_USER key. Allocate this memory using [CoTaskMemAlloc](http://msdn.microsoft.com/library/windows/desktop/ms692727). The calling application is responsible for freeing this memory using [CoTaskMemFree](http://msdn.microsoft.com/library/windows/desktop/ms680722). This parameter should always be initialized to **NULL**, even if the method fails.  
  
 `dwReserved`  
 Reserved for future use. Not currently used.  
  
## Return Value  
 `S_OK` if successful, or **S_FALSE** otherwise. If **S_FALSE**, Internet Explorer or MSHTML will default to its own user options.  
  
## Remarks  
 Override `OnGetOptionKeyPath` to react to the `GetOptionKeyPath` notification from the Microsoft Web Browser control. See [IDocHostUIHandler::GetOptionKeyPath](https://msdn.microsoft.com/en-us/library/aa753258.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)