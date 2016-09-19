---
title: "CWaitCursor::CWaitCursor"
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
ms.assetid: f96cdfeb-9d12-427c-bead-a69fc873d735
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWaitCursor::CWaitCursor
To display a wait cursor, just declare a `CWaitCursor` object before the code that performs the lengthy operation.  
  
## Syntax  
  
```  
  
CWaitCursor( );  
  
```  
  
## Remarks  
 The constructor automatically causes the wait cursor to be displayed.  
  
 When the object goes out of scope (at the end of the block in which the `CWaitCursor` object is declared), its destructor sets the cursor to the previous cursor. In other words, the object performs the necessary clean-up automatically.  
  
 You can take advantage of the fact that the destructor is called at the end of the block (which might be before the end of the function) to make the wait cursor active in only part of your function. This technique is shown in the second example below.  
  
> [!NOTE]
>  Because of how their constructors and destructors work, `CWaitCursor` objects are always declared as local variables — they're never declared as global variables, nor are they allocated with **new**.  
  
## Example  
 [!CODE [NVC_MFCWindowing#63](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#63)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWaitCursor Class](../vs140/CWaitCursor-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWaitCursor::Restore](../vs140/CWaitCursor--Restore.md)   
 [CCmdTarget::BeginWaitCursor](../vs140/CCmdTarget--BeginWaitCursor.md)   
 [CCmdTarget::EndWaitCursor](../vs140/CCmdTarget--EndWaitCursor.md)