---
title: "CDC::GetOutputTabbedTextExtent"
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
ms.assetid: a29c05ed-fae4-4ec8-b360-2c79ac5fbd31
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetOutputTabbedTextExtent
Call this member function to compute the width and height of a character string using [m_hDC](../vs140/CDC--m_hDC.md), the output device context.  
  
## Syntax  
  
```  
  
      CSize GetOutputTabbedTextExtent(  
   LPCTSTR lpszString,  
   int nCount,  
   int nTabPositions,  
   LPINT lpnTabStopPositions   
) const;  
CSize GetOutputTabbedTextExtent(  
   const CString& str,  
   int nTabPositions,  
   LPINT lpnTabStopPositions   
) const;  
```  
  
#### Parameters  
 `lpszString`  
 Points to a character string to be measured. You can also pass a [CString](../vs140/CStringT-Class.md) object for this parameter.  
  
 `nCount`  
 Specifies the number of characters in the string. If `nCount` is –1, the length is calculated.  
  
 `nTabPositions`  
 Specifies the number of tab-stop positions in the array pointed to by `lpnTabStopPositions`.  
  
 `lpnTabStopPositions`  
 Points to an array of integers containing the tab-stop positions in logical units. The tab stops must be sorted in increasing order; the smallest x-value should be the first item in the array. Back tabs are not allowed.  
  
 `str`  
 A `CString` object that contains the specified characters to be measured.  
  
## Return Value  
 The dimensions of the string (in logical units) in a [CSize](../vs140/CSize-Class.md) object.  
  
## Remarks  
 If the string contains one or more tab characters, the width of the string is based upon the tab stops specified by `lpnTabStopPositions`. The function uses the currently selected font to compute the dimensions of the string.  
  
 The current clipping region does not offset the width and height returned by the `GetOutputTabbedTextExtent` function.  
  
 Since some devices do not place characters in regular cell arrays (that is, they kern the characters), the sum of the extents of the characters in a string may not be equal to the extent of the string.  
  
 If `nTabPositions` is 0 and `lpnTabStopPositions` is **NULL**, tabs are expanded to eight average character widths. If `nTabPositions` is 1, the tab stops will be separated by the distance specified by the first value in the array to which `lpnTabStopPositions` points. If `lpnTabStopPositions` points to more than a single value, a tab stop is set for each value in the array, up to the number specified by `nTabPositions`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetTextExtent](../vs140/CDC--GetTextExtent.md)   
 [CDC::m_hAttribDC](../vs140/CDC--m_hAttribDC.md)   
 [CDC::m_hDC](../vs140/CDC--m_hDC.md)   
 [CDC::GetTabbedTextExtent](../vs140/CDC--GetTabbedTextExtent.md)   
 [CDC::GetOutputTextExtent](../vs140/CDC--GetOutputTextExtent.md)   
 [CDC::TabbedTextOut](../vs140/CDC--TabbedTextOut.md)   
 [GetTabbedTextExtent](http://msdn.microsoft.com/library/windows/desktop/dd144930)   
 [CSize Class](../vs140/CSize-Class.md)