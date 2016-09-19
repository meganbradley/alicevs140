---
title: "CDocument::OnUpdateFileSendMail"
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
ms.assetid: 2861c621-b49c-419f-ae89-10561cc2b62c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnUpdateFileSendMail
Enables the **ID_FILE_SEND_MAIL** command if mail support (MAPI) is present.  
  
## Syntax  
  
```  
  
      void OnUpdateFileSendMail(  
   CCmdUI* pCmdUI   
);  
```  
  
#### Parameters  
 `pCmdUI`  
 A pointer to the [CCmdUI](../vs140/CCmdUI-Class.md) object associated with the **ID_FILE_SEND_MAIL** command.  
  
## Remarks  
 Otherwise the function removes the **ID_FILE_SEND_MAIL** command from the menu, including separators above or below the menu item as appropriate. MAPI is enabled if MAPI32.DLL is present in the path and, in the [Mail] section of the WIN.INI file, MAPI=1. Most applications put this command on the File menu.  
  
 **CDocument** supports sending your document via mail if mail support (MAPI) is present. See the articles [MAPI Topics](../vs140/MAPI.md) and [MAPI Support in MFC](../vs140/MAPI-Support-in-MFC.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::OnFileSendMail](../vs140/CDocument--OnFileSendMail.md)