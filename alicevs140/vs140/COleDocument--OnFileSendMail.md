---
title: "COleDocument::OnFileSendMail"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 185ea608-ab73-4363-aa1a-6904695c5d99
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::OnFileSendMail
Sends a message via the resident mail host (if any) with the document as an attachment.  
  
## Syntax  
  
```  
  
afx_msg void OnFileSendMail( );  
```  
  
## Remarks  
 `OnFileSendMail` calls `OnSaveDocument` to serialize (save) untitled and modified documents to a temporary file, which is then sent via electronic mail. If the document has not been modified, a temporary file is not needed; the original is sent. `OnFileSendMail` loads MAPI32.DLL if it has not already been loaded.  
  
 Unlike the implementation of `OnFileSendMail` for **CDocument**, this function handles compound files correctly.  
  
 For more information, see the [MAPI Topics](../vs140/MAPI.md) and [MAPI Support in MFC](../vs140/MAPI-Support-in-MFC.md) articles..  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::OnFileSendMail](../vs140/CDocument--OnFileSendMail.md)   
 [CDocument::OnUpdateFileSendMail](../vs140/CDocument--OnUpdateFileSendMail.md)   
 [CDocument::OnSaveDocument](../vs140/CDocument--OnSaveDocument.md)