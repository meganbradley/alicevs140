---
title: "CStockPropImpl::putref_Picture"
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
ms.assetid: 38c575a2-af79-41ee-a6cd-08de00113e0c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::putref_Picture
Call this method to set the picture properties of a graphic (icon, bitmap, or metafile) to be displayed, with a reference count.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE putref_Picture(  
   IPictureDisp* pPicture   
);  
```  
  
#### Parameters  
 `pPicture`  
 A pointer to the picture's properties. See [IPictureDisp](http://msdn.microsoft.com/library/windows/desktop/ms680762) for more details.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 The same as [CStockPropImpl::put_Picture](../vs140/CStockPropImpl--put_Picture.md), but with a reference count.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Picture](../vs140/CStockPropImpl--put_Picture.md)