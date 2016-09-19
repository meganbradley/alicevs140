---
title: "CGdiObject::GetObjectType"
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
ms.assetid: 61a090bc-2ad6-4e59-a1f0-54f846b4047a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGdiObject::GetObjectType
Retrieves the type of the GDI object.  
  
## Syntax  
  
```  
  
UINT GetObjectType( ) const;  
```  
  
## Return Value  
 The type of the object, if successful; otherwise 0. The value can be one of the following:  
  
-   **OBJ_BITMAP** Bitmap  
  
-   **OBJ_BRUSH** Brush  
  
-   **OBJ_FONT** Font  
  
-   **OBJ_PAL** Palette  
  
-   **OBJ_PEN** Pen  
  
-   **OBJ_EXTPEN** Extended pen  
  
-   **OBJ_REGION** Region  
  
-   **OBJ_DC** Device context  
  
-   **OBJ_MEMDC** Memory device context  
  
-   **OBJ_METAFILE** Metafile  
  
-   **OBJ_METADC** Metafile device context  
  
-   **OBJ_ENHMETAFILE** Enhanced metafile  
  
-   **OBJ_ENHMETADC** Enhanced-metafile device context  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CGdiObject Class](../vs140/CGdiObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGdiObject::GetObject](../vs140/CGdiObject--GetObject.md)   
 [CDC::SelectObject](../vs140/CDC--SelectObject.md)