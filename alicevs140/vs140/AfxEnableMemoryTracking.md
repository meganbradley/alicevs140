---
title: "AfxEnableMemoryTracking"
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
ms.assetid: 0a40e0c4-855d-46e2-9577-a8f2346f47db
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxEnableMemoryTracking
Diagnostic memory tracking is normally enabled in the Debug version of MFC.  
  
## Syntax  
  
```  
  
      BOOL AfxEnableMemoryTracking(  
   BOOL bTrack   
);   
```  
  
#### Parameters  
 *bTrack*  
 Setting this value to **TRUE** turns on memory tracking; **FALSE** turns it off.  
  
## Return Value  
 The previous setting of the tracking-enable flag.  
  
## Remarks  
 Use this function to disable tracking on sections of your code that you know are allocating blocks correctly.  
  
 For more information on `AfxEnableMemoryTracking`, see [Debugging MFC Applications](../vs140/MFC-Debugging-Techniques.md).  
  
> [!NOTE]
>  This function works only in the Debug version of MFC.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#24](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#24)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)