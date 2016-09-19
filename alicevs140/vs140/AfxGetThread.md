---
title: "AfxGetThread"
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
ms.topic: article
ms.assetid: 75e7a519-c7e2-4ab0-ae05-20bb53e5df08
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetThread
Call this function to get a pointer to the [CWinThread](../vs140/CWinThread-Class.md) object representing the currently executing thread.  
  
## Syntax  
  
```  
  
CWinThread* AfxGetThread( );  
```  
  
## Return Value  
 Pointer to the currently executing thread; otherwise **NULL**.  
  
## Remarks  
 Must be called from within the desired thread.  
  
> [!NOTE]
>  If you are porting an MFC project calling `AfxGetThread` from Visual C++ versions 4.2, 5.0, or 6.0, `AfxGetThread` calls [AfxGetApp](../vs140/AfxGetApp.md) if no thread is found. In Visual C+ .NET and later, `AfxGetThread` returns **NULL** if no thread was found. If you want the application thread, you must call `AfxGetApp`.  
  
## Example  
 [!CODE [NVC_MFCWindowing#132](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#132)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxBeginThread](../vs140/AfxBeginThread.md)