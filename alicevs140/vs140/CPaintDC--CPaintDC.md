---
title: "CPaintDC::CPaintDC"
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
ms.assetid: 85ad20f4-f348-4bd8-8c94-9a9da802fe5f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaintDC::CPaintDC
Constructs a `CPaintDC` object, prepares the application window for painting, and stores the [PAINTSTRUCT](../vs140/PAINTSTRUCT-Structure.md) structure in the [m_ps](../vs140/CPaintDC--m_ps.md) member variable.  
  
## Syntax  
  
```  
  
      explicit CPaintDC(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 Points to the `CWnd` object to which the `CPaintDC` object belongs.  
  
## Remarks  
 An exception (of type `CResourceException`) is thrown if the Windows [GetDC](http://msdn.microsoft.com/library/windows/desktop/dd144871) call fails. A device context may not be available if Windows has already allocated all of its available device contexts. Your application competes for the five common display contexts available at any given time under Windows.  
  
## Example  
 [!CODE [NVC_MFCDocView#97](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#97)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPaintDC Class](../vs140/CPaintDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)