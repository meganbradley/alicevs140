---
title: "Searching and Sorting"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 15e984f0-e155-46f5-8542-51c458792f54
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Searching and Sorting
Use the following functions for searching and sorting.  
  
### Searching and Sorting Functions  
  
|Function|Search or Sort|.NET Framework equivalent|  
|--------------|--------------------|-------------------------------|  
|[bsearch](../vs140/bsearch.md)|Binary search|[System::Collections::ArrayList::BinarySearch](https://msdn.microsoft.com/en-us/library/system.collections.arraylist.binarysearch.aspx)|  
|[bsearch_s](../Topic/bsearch_s.md)|A more secure version of `bsearch`.|[System::Collections::ArrayList::BinarySearch](https://msdn.microsoft.com/en-us/library/system.collections.arraylist.binarysearch.aspx)|  
|[_lfind](../vs140/_lfind.md)|Linear search for given value|[System::Collections::ArrayList::Contains](https://msdn.microsoft.com/en-us/library/system.collections.arraylist.contains.aspx)|  
|[_lfind_s](../Topic/_lfind_s.md)|A more secure version of `_lfind`|[System::Collections::ArrayList::Contains](https://msdn.microsoft.com/en-us/library/system.collections.arraylist.contains.aspx)|  
|[_lsearch](../vs140/_lsearch.md)|Linear search for given value, which is added to array if not found|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[_lsearch_s](../vs140/_lsearch_s.md)|A more secure version of `_lsearch`|Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).|  
|[qsort](../vs140/qsort.md)|Quick sort|[System::Collections::ArrayList::Sort](https://msdn.microsoft.com/en-us/library/system.collections.arraylist.sort.aspx)|  
|[qsort_s](../Topic/qsort_s.md)|A more secure version of `qsort`|[System::Collections::ArrayList::Sort](https://msdn.microsoft.com/en-us/library/system.collections.arraylist.sort.aspx)|  
  
## See Also  
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)