---
title: "CPictureHolder::CreateFromMetafile"
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
ms.assetid: 7252ec30-ddfd-4108-8be1-1238108731be
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPictureHolder::CreateFromMetafile
Uses a metafile to initialize the picture object in a `CPictureHolder`.  
  
## Syntax  
  
```  
  
      BOOL CreateFromMetafile(  
   HMETAFILE hmf,  
   int xExt,  
   int yExt,  
   BOOL bTransferOwnership = FALSE   
);  
```  
  
#### Parameters  
 `hmf`  
 Handle to the metafile used to create the `CPictureHolder` object.  
  
 *xExt*  
 X extent of the picture.  
  
 *yExt*  
 Y extent of the picture.  
  
 `bTransferOwnership`  
 Indicates whether the picture object will take ownership of the metafile object.  
  
## Return Value  
 Nonzero if the object is successfully created; otherwise 0.  
  
## Remarks  
 If `bTransferOwnership` is **TRUE**, the caller should not use the metafile object in any way after this call returns. If `bTransferOwnership` is **FALSE**, the caller is responsible for ensuring that the metafile object remains valid for the lifetime of the picture object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPictureHolder Class](../vs140/CPictureHolder-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPictureHolder::CreateEmpty](../vs140/CPictureHolder--CreateEmpty.md)   
 [CPictureHolder::CreateFromBitmap](../vs140/CPictureHolder--CreateFromBitmap.md)   
 [CPictureHolder::CreateFromIcon](../vs140/CPictureHolder--CreateFromIcon.md)