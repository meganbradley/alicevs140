---
title: "CRichEditCtrl::FindText"
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
ms.assetid: d7eee081-412d-4def-a583-3bf0c48cb5e1
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::FindText
Finds text within the rich edit control.  
  
## Syntax  
  
```  
  
      long FindText(  
   DWORD dwFlags,  
   FINDTEXTEX* pFindText   
) const;  
```  
  
#### Parameters  
 `dwFlags`  
 For a list of possible values, see `wParam` in [EM_FINDTEXTEXT](http://msdn.microsoft.com/library/windows/desktop/bb788011) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 *pFindText*  
 Pointer to the [FINDTEXTEX](http://msdn.microsoft.com/library/windows/desktop/bb787909) structure giving the parameters for the search and returning the range where the match was found.  
  
## Return Value  
 Zero-based character position of the next match; – 1 if there are no more matches.  
  
## Remarks  
 You can search either up or down by setting the proper range parameters in the [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) structure within the **FINDTEXTEX** structure.  
  
 For more information, see [EM_FINDTEXTEX](http://msdn.microsoft.com/library/windows/desktop/bb788011) message and [FINDTEXTEX](http://msdn.microsoft.com/library/windows/desktop/bb787909) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#9)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::SetSel](../vs140/CRichEditCtrl--SetSel.md)