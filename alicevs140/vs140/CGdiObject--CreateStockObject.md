---
title: "CGdiObject::CreateStockObject"
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
ms.assetid: 9687aa6a-b33b-47b5-847f-df78c717b8e7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGdiObject::CreateStockObject
Retrieves a handle to one of the predefined stock Windows GDI pens, brushes, or fonts, and attaches the GDI object to the `CGdiObject` object.  
  
## Syntax  
  
```  
  
      BOOL CreateStockObject(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 A constant specifying the type of stock object desired. See the parameter *fnObject* for [GetStockObject](http://msdn.microsoft.com/library/windows/desktop/dd144925) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a description of appropriate values.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 Call this function with one of the derived classes that corresponds to the Windows GDI object type, such as `CPen` for a stock pen.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CGdiObject Class](../vs140/CGdiObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPen::CPen](../vs140/CPen--CPen.md)   
 [CBrush::CBrush](../vs140/CBrush--CBrush.md)   
 [CFont::CFont](../vs140/CFont--CFont.md)   
 [CPalette::CPalette](../vs140/CPalette--CPalette.md)