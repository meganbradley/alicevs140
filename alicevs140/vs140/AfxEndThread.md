---
title: "AfxEndThread"
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
ms.assetid: b8215409-7724-4159-9156-16b543443b99
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxEndThread
Call this function to terminate the currently executing thread.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxEndThread(  
   UINT nExitCode,  
   BOOL bDelete = TRUE   
);  
```  
  
#### Parameters  
 *nExitCode*  
 Specifies the exit code of the thread.  
  
 *bDelete*  
 Deletes the thread object from memory.  
  
## Remarks  
 Must be called from within the thread to be terminated.  
  
 For more information on `AfxEndThread`, see the article [Multithreading: Terminating Threads](../vs140/Multithreading--Terminating-Threads.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxBeginThread](../vs140/AfxBeginThread.md)