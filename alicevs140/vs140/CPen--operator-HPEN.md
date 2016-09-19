---
title: "CPen::operator HPEN"
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
ms.assetid: 8930c124-5b12-46a3-9217-a7cd7b9d3508
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPen::operator HPEN
Gets the attached Windows GDI handle of the `CPen` object.  
  
## Syntax  
  
```  
  
operator HPEN( ) const;  
  
```  
  
## Return Value  
 If successful, a handle to the Windows GDI object represented by the `CPen` object; otherwise **NULL**.  
  
## Remarks  
 This operator is a casting operator, which supports direct use of an `HPEN` object.  
  
 For more information about using graphic objects, see the article [Graphic Objects](http://msdn.microsoft.com/library/windows/desktop/dd144962) in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocView#104](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#104)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPen Class](../vs140/CPen-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)