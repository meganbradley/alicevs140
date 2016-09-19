---
title: "CPictureHolder::CreateFromIcon"
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
ms.assetid: 284c4cd2-5506-472b-8a81-b56e5d9a8cde
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPictureHolder::CreateFromIcon
Uses an icon to initialize the picture object in a `CPictureHolder`.  
  
## Syntax  
  
```  
  
      BOOL CreateFromIcon(  
   UINT idResource   
);  
BOOL CreateFromIcon(  
   HICON hIcon,  
   BOOL bTransferOwnership = FALSE   
);  
```  
  
#### Parameters  
 `idResource`  
 Resource ID of a bitmap resource.  
  
 `hIcon`  
 Handle to the icon from which the `CPictureHolder` object is created.  
  
 `bTransferOwnership`  
 Indicates whether the picture object will take ownership of the icon object.  
  
## Return Value  
 Nonzero if the object is successfully created; otherwise 0.  
  
## Remarks  
 If `bTransferOwnership` is **TRUE**, the caller should not use the icon object in any way after this call returns. If `bTransferOwnership` is **FALSE**, the caller is responsible for ensuring that the icon object remains valid for the lifetime of the picture object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPictureHolder Class](../vs140/CPictureHolder-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPictureHolder::CreateEmpty](../vs140/CPictureHolder--CreateEmpty.md)   
 [CPictureHolder::CreateFromBitmap](../vs140/CPictureHolder--CreateFromBitmap.md)   
 [CPictureHolder::CreateFromMetafile](../vs140/CPictureHolder--CreateFromMetafile.md)