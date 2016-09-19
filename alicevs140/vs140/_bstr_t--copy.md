---
title: "_bstr_t::copy"
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
ms.topic: language-reference
ms.assetid: 00ba7311-e82e-4a79-8106-5329fa2f869a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _bstr_t::copy
**Microsoft Specific**  
  
 Constructs a copy of the encapsulated `BSTR`.  
  
## Syntax  
  
```  
  
      BSTR copy(  
  bool fCopy = true  
) const;  
```  
  
#### Parameters  
 `fCopy`  
 If **true**, **copy** returns a copy of the contained `BSTR`, otherwise **copy** returns the actual BSTR.  
  
## Remarks  
 Returns a newly allocated copy of the encapsulated `BSTR` object.  
  
## Example  
  
```  
STDMETHODIMP CAlertMsg::get_ConnectionStr(BSTR *pVal){ //  m_bsConStr is _bstr_t  
   *pVal = m_bsConStr.copy();  
}  
```  
  
 **END Microsoft Specific**  
  
## See Also  
 [_bstr_t Class](../vs140/_bstr_t-Class.md)