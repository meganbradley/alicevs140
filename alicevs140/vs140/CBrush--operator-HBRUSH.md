---
title: "CBrush::operator HBRUSH"
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
ms.assetid: 46a21e6d-5be1-4260-9443-88f93b70d605
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBrush::operator HBRUSH
Use this operator to get the attached Windows GDI handle of the `CBrush` object.  
  
## Syntax  
  
```  
  
operator HBRUSH( ) const;  
  
```  
  
## Return Value  
 If successful, a handle to the Windows GDI object represented by the `CBrush` object; otherwise **NULL**.  
  
## Remarks  
 This operator is a casting operator, which supports direct use of an `HBRUSH` object.  
  
 For more information about using graphic objects, see [Graphic Objects](http://msdn.microsoft.com/library/windows/desktop/dd144962) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#28)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CBrush Class](../vs140/CBrush-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)