---
title: "CMemoryState::DumpStatistics"
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
ms.assetid: 90d5f281-b92f-4725-a996-23ab94cf4b5d
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMemoryState::DumpStatistics
Prints a concise memory statistics report from a `CMemoryState` object that is filled by the [Difference](../vs140/CMemoryState--Difference.md) member function.  
  
## Syntax  
  
```  
  
void DumpStatistics( ) const;  
```  
  
## Remarks  
 The report, which is printed on the [afxDump](../vs140/afxDump--CDumpContext-in-MFC-.md) device, shows the following:  
  
 A sample report gives information on the number (or amount) of:  
  
-   free blocks  
  
-   normal blocks  
  
-   CRT blocks  
  
-   ignore blocks  
  
-   client blocks  
  
-   maximum memory used by the program at any one time (in bytes)  
  
-   total memory currently used by the program (in bytes)  
  
 Free blocks are the number of blocks whose deallocation was delayed if `afxMemDF` was set to **delayFreeMemDF**. For more information, see [afxMemDF](../vs140/afxMemDF.md), in the "MFC Macros and Globals" section. See [Types of Blocks on the Debug Heap](assetId:///db2e7f62-0679-4b39-a23f-26f2c2f407c5) for more information on these block types.  
  
## Example  
 The following code should be placed in *projname*App.cpp. Define the following global variables:  
  
 [!CODE [NVC_MFC_Utilities#40](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#40)]  
  
 In the `InitInstance` function, add the line:  
  
 [!CODE [NVC_MFC_Utilities#41](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#41)]  
  
 Add a handler for the `ExitInstance` function and use the following code:  
  
 [!CODE [NVC_MFC_Utilities#42](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#42)]  
  
 You can now run the program in Debug mode to see the output of the `DumpStatistics` function.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CMemoryState Structure](../vs140/CMemoryState-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)