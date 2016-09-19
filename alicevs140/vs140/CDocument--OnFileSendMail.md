---
title: "CDocument::OnFileSendMail"
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
ms.assetid: 85545440-a581-4d7d-b950-dae789aa9d3f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::OnFileSendMail
Sends a message via the resident mail host (if any) with the document as an attachment.  
  
## Syntax  
  
```  
  
void OnFileSendMail( );  
```  
  
## Remarks  
 `OnFileSendMail` calls [OnSaveDocument](../vs140/CDocument--OnSaveDocument.md) to serialize (save) untitled and modified documents to a temporary file, which is then sent via electronic mail. If the document has not been modified, a temporary file is not needed; the original is sent. `OnFileSendMail` loads MAPI32.DLL if it has not already been loaded.  
  
 A special implementation of `OnFileSendMail` for [COleDocument](../vs140/COleDocument-Class.md) handles compound files correctly.  
  
 **CDocument** supports sending your document via mail if mail support (MAPI) is present. See the articles [MAPI Topics](../vs140/MAPI.md) and [MAPI Support in MFC](../vs140/MAPI-Support-in-MFC.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::OnUpdateFileSendMail](../vs140/CDocument--OnUpdateFileSendMail.md)   
 [COleDocument::OnFileSendMail](../vs140/COleDocument--OnFileSendMail.md)   
 [CDocument::OnSaveDocument](../vs140/CDocument--OnSaveDocument.md)