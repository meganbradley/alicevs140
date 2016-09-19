---
title: "CRichEditView::OnPasteNativeObject"
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
ms.assetid: f3fe0f3c-ad8f-4051-984f-a7a20d6994d9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::OnPasteNativeObject
Use this function to load native data from an embedded item.  
  
## Syntax  
  
```  
  
      virtual BOOL OnPasteNativeObject(  
   LPSTORAGE lpStg   
);  
```  
  
#### Parameters  
 *lpStg*  
 Pointer to an [IStorage](http://msdn.microsoft.com/library/windows/desktop/aa380015) object.  
  
## Return Value  
 Nonzero if successful; otherwise, 0;  
  
## Remarks  
 Typically, you would do this by creating a [COleStreamFile](../vs140/COleStreamFile-Class.md) around the `IStorage`. The `COleStreamFile` can be attached to an archive and [CObject::Serialize](../vs140/CObject--Serialize.md) called to load the data.  
  
 This is an advanced overridable.  
  
 For more information, see [IStorage](http://msdn.microsoft.com/library/windows/desktop/aa380015) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleStreamFile Class](../vs140/COleStreamFile-Class.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)   
 [CArchive Class](../vs140/CArchive-Class.md)