---
title: "CRichEditCtrl::GetLine"
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
ms.assetid: b033c987-e263-43f4-8bd7-cbac60d90796
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetLine
Retrieves a line of text from this `CRichEditCtrl` object.  
  
## Syntax  
  
```  
  
      int GetLine(  
   int nIndex,  
   LPTSTR lpszBuffer   
) const;  
int GetLine(  
   int nIndex,  
   LPTSTR lpszBuffer,  
   int nMaxLength   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Zero-based index of the line to retrieve.  
  
 `lpszBuffer`  
 Points to the buffer to receive the text. The first word of the buffer must specify the maximum number of bytes that can be copied into the buffer.  
  
 `nMaxLength`  
 Maximum number of characters that can be copied into `lpszBuffer`. The second form of `GetLine` places this value into the first word of the buffer specified by `lpszBuffer`.  
  
## Return Value  
 The number of characters copied into `lpszBuffer`.  
  
## Remarks  
 The copied line does not contain a terminating null character.  
  
> [!NOTE]
>  Because the first word of the buffer stores the number of characters to be copied, make sure that your buffer is at least 4 bytes long.  
  
 For more information, see [EM_GETLINE](http://msdn.microsoft.com/library/windows/desktop/bb761584) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [GetLineCount](../vs140/CRichEditCtrl--GetLineCount.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::LineLength](../vs140/CRichEditCtrl--LineLength.md)