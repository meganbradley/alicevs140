---
title: "CPropExchange::ExchangeFontProp"
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
ms.assetid: 664d7547-6287-4143-af10-7792dee7eb77
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropExchange::ExchangeFontProp
Exchanges a font property between a storage medium and the control.  
  
## Syntax  
  
```  
  
      virtual BOOL ExchangeFontProp(  
   LPCTSTR pszPropName,  
   CFontHolder& font,  
   const FONTDESC* pFontDesc,  
   LPFONTDISP pFontDispAmbient   
) = 0;  
```  
  
#### Parameters  
 `pszPropName`  
 The name of the property being exchanged.  
  
 `font`  
 A reference to a [CFontHolder](../vs140/CFontHolder-Class.md) object that contains the font property.  
  
 `pFontDesc`  
 A pointer to a [FONTDESC](http://msdn.microsoft.com/library/windows/desktop/ms692782) structure containing values for initializing the default state of the font property when `pFontDispAmbient` is **NULL**.  
  
 `pFontDispAmbient`  
 A pointer to the **IFontDisp** interface of a font to be used for initializing the default state of the font property.  
  
## Return Value  
 Nonzero if the exchange was successful; 0 if unsuccessful.  
  
## Remarks  
 If the font property is being loaded from the medium to the control, the font's characteristics are retrieved from the medium and the `CFontHolder` object referenced by `font` is initialized with them. If the font property is being stored, the characteristics in the font object are written to the medium.  
  
 The functions **CArchivePropExchange::ExchangeFontProp**, **CResetPropExchange::ExchangeFontProp**, and **CPropsetPropExchange::ExchangeFontProp** override this pure virtual function.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CPropExchange Class](../vs140/CPropExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [CPropExchange::ExchangeBlobProp](../vs140/CPropExchange--ExchangeBlobProp.md)   
 [CPropExchange::ExchangePersistentProp](../vs140/CPropExchange--ExchangePersistentProp.md)   
 [CPropExchange::ExchangeProp](../vs140/CPropExchange--ExchangeProp.md)