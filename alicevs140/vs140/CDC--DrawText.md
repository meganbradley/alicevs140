---
title: "CDC::DrawText"
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
ms.assetid: de687c9f-55f7-4e4e-8cb6-13fd6d9e7327
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::DrawText
Call this member function to format text in the given rectangle. To specify additional formatting options, use [CDC::DrawTextEx](../vs140/CDC--DrawTextEx.md).  
  
## Syntax  
  
```  
  
      virtual int DrawText(  
   LPCTSTR lpszString,  
   int nCount,  
   LPRECT lpRect,  
   UINT nFormat   
);  
int DrawText(  
   const CString& str,  
   LPRECT lpRect,  
   UINT nFormat   
);  
```  
  
#### Parameters  
 `lpszString`  
 Points to the string to be drawn. If `nCount` is –1, the string must be null-terminated.  
  
 `nCount`  
 Specifies the number of chars in the string. If `nCount` is –1, then `lpszString` is assumed to be a long pointer to a null-terminated string and `DrawText` computes the character count automatically.  
  
 `lpRect`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or [CRect](../vs140/CRect-Class.md) object that contains the rectangle (in logical coordinates) in which the text is to be formatted.  
  
 `str`  
 A [CString](../vs140/CStringT-Class.md) object that contains the specified characters to be drawn.  
  
 `nFormat`  
 Specifies the method of formatting the text. It can be any combination of the values described for the `uFormat` parameter in [DrawText](http://msdn.microsoft.com/library/windows/desktop/dd162498) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. (combine using the bitwise OR operator):  
  
> [!NOTE]
>  Some `uFormat` flag combinations can cause the passed string to be modified. Using **DT_MODIFYSTRING** with either **DT_END_ELLIPSIS** or **DT_PATH_ELLIPSIS** may cause the string to be modified, causing an assertion in the `CString` override. The values `DT_CALCRECT`, `DT_EXTERNALLEADING`, **DT_INTERNAL**, `DT_NOCLIP`, and `DT_NOPREFIX` cannot be used with the `DT_TABSTOP` value.  
  
## Return Value  
 The height of the text if the function is successful.  
  
## Remarks  
 It formats text by expanding tabs into appropriate spaces, aligning text to the left, right, or center of the given rectangle, and breaking text into lines that fit within the given rectangle. The type of formatting is specified by `nFormat`.  
  
 This member function uses the device context's selected font, text color, and background color to draw the text. Unless the `DT_NOCLIP` format is used, `DrawText` clips the text so that the text does not appear outside the given rectangle. All formatting is assumed to have multiple lines unless the `DT_SINGLELINE` format is given.  
  
 If the selected font is too large for the specified rectangle, the `DrawText` member function does not attempt to substitute a smaller font.  
  
 If the `DT_CALCRECT` flag is specified, the rectangle specified by `lpRect` will be updated to reflect the width and height needed to draw the text.  
  
 If the **TA_UPDATECP** text-alignment flag has been set (see [CDC::SetTextAlign](../vs140/CDC--SetTextAlign.md)), `DrawText` will display text starting at the current position, rather than at the left of the given rectangle. `DrawText` will not wrap text when the **TA_UPDATECP** flag has been set (that is, the `DT_WORDBREAK` flag will have no effect).  
  
 The text color may be set by [CDC::SetTextColor](../vs140/CDC--SetTextColor.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetTextColor](../vs140/CDC--SetTextColor.md)   
 [CDC::ExtTextOut](../vs140/CDC--ExtTextOut.md)   
 [CDC::TabbedTextOut](../vs140/CDC--TabbedTextOut.md)   
 [CDC::TextOut](../vs140/CDC--TextOut.md)   
 [DrawText](http://msdn.microsoft.com/library/windows/desktop/dd162498)   
 [RECT Structure](../vs140/RECT-Structure.md)   
 [CDC::SetTextAlign](../vs140/CDC--SetTextAlign.md)