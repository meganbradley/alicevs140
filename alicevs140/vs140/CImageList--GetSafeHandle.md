---
title: "CImageList::GetSafeHandle"
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
ms.assetid: 523ed19a-ed57-40aa-a145-1c254500dca3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::GetSafeHandle
Call this function to retrieve the **m_hImageList** data member.  
  
## Syntax  
  
```  
  
HIMAGELIST GetSafeHandle( ) const;  
```  
  
## Return Value  
 A handle to the attached image list; otherwise **NULL** if no object is attached.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#15)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::Attach](../vs140/CImageList--Attach.md)   
 [CImageList::Detach](../vs140/CImageList--Detach.md)   
 [CImageList::m_hImageList](../vs140/CImageList--m_hImageList.md)