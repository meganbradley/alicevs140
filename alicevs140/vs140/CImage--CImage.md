---
title: "CImage::CImage"
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
ms.assetid: 6d9dbe81-bb4d-42db-b52b-5f18ff241632
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::CImage
Constructs a `CImage` object.  
  
## Syntax  
  
```  
  
CImage( ) throw( );  
  
```  
  
## Remarks  
 Once you have constructed the object, call [Create](../vs140/CImage--Create.md), [Load](../vs140/CImage--Load.md), [LoadFromResource](../vs140/CImage--LoadFromResource.md), or [Attach](../vs140/CImage--Attach.md) to attach a bitmap to the object.  
  
 **Note** In Visual Studio, this class keeps a count of the number of `CImage` objects created. Whenever the count goes to 0, the function [GdiplusShutdown](_gdiplus_func_gdiplusshutdown_) is automatically called to release resources used by GDI+. This ensures that any `CImage` objects created directly or indirectly by DLLs are always destroyed properly and that **GdiplusShutdown** is not called from DllMain.  
  
 Using global `CImage` objects in a DLL is not recommended. If you need to use a global `CImage` object in a DLL, call [CImage::ReleaseGDIPlus](../vs140/CImage--ReleaseGDIPlus.md) to explicitly release resources used by GDI+.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)