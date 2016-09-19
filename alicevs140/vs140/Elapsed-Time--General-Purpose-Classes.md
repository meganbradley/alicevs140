---
title: "Elapsed Time: General-Purpose Classes"
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
ms.assetid: e5c5d3d2-ce1d-409e-875c-98848434e716
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Elapsed Time: General-Purpose Classes
The following procedure shows how to calculate the difference between two `CTime` objects and get a `CTimeSpan` result.  
  
#### To calculate elapsed time  
  
1.  Use the `CTime` and `CTimeSpan` objects to calculate the elapsed time, as follows:  
  
     [!CODE [NVC_ATLMFC_Utilities#174](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#174)]  
  
     Once you have calculated `elapsedTime`, you can use the member functions of `CTimeSpan` to extract the components of the elapsed-time value.  
  
## See Also  
 [Date and Time: General-Purpose Classes](../vs140/Date-and-Time--General-Purpose-Classes.md)