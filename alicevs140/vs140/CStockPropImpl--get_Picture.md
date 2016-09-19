---
title: "CStockPropImpl::get_Picture"
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
ms.assetid: 8fe57ebb-7e66-4fdf-b6ca-fac1697a2c22
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_Picture
Call this method to get a pointer to the picture properties of a graphic (icon, bitmap, or metafile) to be displayed.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Picture(  
   IPictureDisp** ppPicture   
);  
```  
  
#### Parameters  
 `ppPicture`  
 Variable that receives a pointer to the picture's properties. See [IPictureDisp](http://msdn.microsoft.com/library/windows/desktop/ms680762) for more details.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Picture](../vs140/CStockPropImpl--put_Picture.md)