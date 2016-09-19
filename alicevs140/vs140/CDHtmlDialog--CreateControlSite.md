---
title: "CDHtmlDialog::CreateControlSite"
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
ms.assetid: 5ffe6fa3-d1bc-45d9-bab5-53f14cf1496e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::CreateControlSite
Overridable used to create a control site instance to host the WebBrowser control on the dialog.  
  
## Syntax  
  
```  
  
      virtual BOOL CreateControlSite(  
   COleControlContainer* pContainer,  
   COleControlSite** ppSite,  
   UINT /* nID */,  
   REFCLSID /* clsid */   
);  
```  
  
#### Parameters  
 `pContainer`  
 A pointer to the [COleControlContainer](../vs140/COleControlContainer-Class.md) object  
  
 `ppSite`  
 A pointer to a pointer to a [COleControlSite](../vs140/COleControlSite-Class.md).  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 You can override this member function to return an instance of your own control site class.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)