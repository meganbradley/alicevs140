---
title: "CRichEditCtrl::GetTextRange"
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
ms.assetid: eca22cbe-da17-49ab-b7bb-45dbca44bef5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::GetTextRange
Gets the specified range of characters.  
  
## Syntax  
  
```  
  
      int GetTextRange(  
   int nFirst,  
   int nLast,  
   CString& refString   
) const;  
```  
  
#### Parameters  
 `nFirst`  
 The character position index immediately preceding the first character in the range.  
  
 `nLast`  
 The character position immediately following the last character in the range.  
  
 `refString`  
 A reference to a [CString](../vs140/CStringT-Class.md) object that will receive the text.  
  
## Return Value  
 The number of characters copied, not including the terminating null character.  
  
## Remarks  
 For more information, see [EM_GETTEXTRANGE](http://msdn.microsoft.com/library/windows/desktop/bb774199) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `GetTextRange` supports the Rich Edit 2.0 functionality. See [About Rich Edit Controls](http://msdn.microsoft.com/library/windows/desktop/bb787873) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]for more information.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::GetTextLength](../vs140/CRichEditCtrl--GetTextLength.md)   
 [CRichEditCtrl::GetTextLengthEx](../vs140/CRichEditCtrl--GetTextLengthEx.md)