---
title: "CImageList::FromHandle"
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
ms.assetid: 482db815-e383-4f87-b9db-51fe3e38ac07
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::FromHandle
Returns a pointer to a `CImageList` object when given a handle to an image list.  
  
## Syntax  
  
```  
  
      static CImageList* PASCAL FromHandle(  
   HIMAGELIST hImageList   
);  
```  
  
#### Parameters  
 `hImageList`  
 Specifies the image list.  
  
## Return Value  
 A pointer to a `CImageList` object if successful; otherwise **NULL**.  
  
## Remarks  
 If a `CImageList` is not already attached to the handle, a temporary `CImageList` object is created and attached. This temporary `CImageList` object is valid only until the next time the application has idle time in its event loop, at which time all temporary objects are deleted.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#13)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::FromHandlePermanent](../vs140/CImageList--FromHandlePermanent.md)