---
title: "COleClientItem::GetIconFromRegistry"
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
ms.assetid: 3a0d9294-58bd-4ba8-9f0e-aec0e106c3a7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetIconFromRegistry
Call this member function to retrieve a handle to an icon resource associated with the server of a particular CLSID.  
  
## Syntax  
  
```  
  
      HICON GetIconFromRegistry( ) const;   
static HICON GetIconFromRegistry(  
   CLSID& clsid   
);  
```  
  
#### Parameters  
 `clsid`  
 A reference to the CLSID for the server associated with the icon.  
  
## Return Value  
 A valid handle to the icon resource, or **NULL** if the server's icon, or a default icon, can't be found.  
  
## Remarks  
 This member function will not start the server or obtain an icon dynamically, even if the server is already running. Instead, this member function opens the server's executable image and retrieves the static icon associated with the server as it was registered.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)