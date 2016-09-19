---
title: "CDC::SelectObject"
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
ms.assetid: b23aa641-a6bb-43cd-bcd9-9171f81f97f3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SelectObject
Selects an object into the device context.  
  
## Syntax  
  
```  
  
      CPen* SelectObject(  
   CPen* pPen   
);  
CBrush* SelectObject(  
   CBrush* pBrush   
);  
virtual CFont* SelectObject(  
   CFont* pFont   
);  
CBitmap* SelectObject(  
   CBitmap* pBitmap   
);  
int SelectObject(  
   CRgn* pRgn   
);  
CGdiObject* SelectObject(  
   CGdiObject* pObject  
);  
```  
  
#### Parameters  
 *pPen*  
 A pointer to a [CPen](../vs140/CPen-Class.md) object to be selected.  
  
 `pBrush`  
 A pointer to a [CBrush](../vs140/CBrush-Class.md) object to be selected.  
  
 `pFont`  
 A pointer to a [CFont](../vs140/CFont-Class.md) object to be selected.  
  
 `pBitmap`  
 A pointer to a [CBitmap](../vs140/CBitmap-Class.md) object to be selected.  
  
 `pRgn`  
 A pointer to a [CRgn](../vs140/CRgn-Class.md) object to be selected.  
  
 `pObject`  
 A pointer to a [CGdiObject](../vs140/CGdiObject-Class.md) object to be selected.  
  
## Return Value  
 A pointer to the object being replaced. This is a pointer to an object of one of the classes derived from `CGdiObject`, such as `CPen`, depending on which version of the function is used. The return value is **NULL** if there is an error. This function may return a pointer to a temporary object. This temporary object is only valid during the processing of one Windows message. For more information, see `CGdiObject::FromHandle`.  
  
 The version of the member function that takes a region parameter performs the same task as the `SelectClipRgn` member function. Its return value can be any of the following:  
  
-   **COMPLEXREGION** New clipping region has overlapping borders.  
  
-   **ERROR** Device context or region is not valid.  
  
-   **NULLREGION** New clipping region is empty.  
  
-   **SIMPLEREGION** New clipping region has no overlapping borders.  
  
## Remarks  
 Class `CDC` provides five versions specialized for particular kinds of GDI objects, including pens, brushes, fonts, bitmaps, and regions. The newly selected object replaces the previous object of the same type. For example, if `pObject` of the general version of `SelectObject` points to a [CPen](../vs140/CPen-Class.md) object, the function replaces the current pen with the pen specified by `pObject`.  
  
 An application can select a bitmap into memory device contexts only and into only one memory device context at a time. The format of the bitmap must either be monochrome or compatible with the device context; if it is not, `SelectObject` returns an error.  
  
 For Windows 3.1 and later, the `SelectObject` function returns the same value whether it is used in a metafile or not. Under previous versions of Windows, `SelectObject` returned a nonzero value for success and 0 for failure when it was used in a metafile.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGdiObject::DeleteObject](../vs140/CGdiObject--DeleteObject.md)   
 [CGdiObject::FromHandle](../vs140/CGdiObject--FromHandle.md)   
 [CDC::SelectClipRgn](../vs140/CDC--SelectClipRgn.md)   
 [CDC::SelectPalette](../vs140/CDC--SelectPalette.md)   
 [SelectObject](http://msdn.microsoft.com/library/windows/desktop/dd162957)