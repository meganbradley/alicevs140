---
title: "IDebugExpressionEvaluator::Parse"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e6e31b3a-63a7-4293-bcda-267eb78dffb6
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExpressionEvaluator::Parse
This method converts an expression string to a parsed expression.  
  
## Syntax  
  
```cpp#  
HRESULT Parse(   
   LPCOLESTR                upstrExpression,  
   PARSEFLAGS               dwFlags,  
   UINT                     nRadix,  
   BSTR*                    pbstrError,  
   UINT*                    pichError,  
   IDebugParsedExpression** ppParsedExpression  
);  
```  
  
```c#  
int Parse(  
   string                     upstrExpression,   
   enum_PARSEFLAGS            dwFlags,   
   uint                       nRadix,   
   out string                 pbstrError,   
   out uint                   pichError,   
   out IDebugParsedExpression ppParsedExpression  
);  
```  
  
#### Parameters  
 `upstrExpression`  
 [in] The expression string to be parsed.  
  
 `dwFlags`  
 [in] A collection of [PARSEFLAGS](../vs140/PARSEFLAGS.md) constants that determine how the expression is to be parsed.  
  
 `nRadix`  
 [in] Radix to be used to interpret any numerical information.  
  
 `pbstrError`  
 [out] Returns the  error as human-readable text.  
  
 `pichError`  
 [out] Returns the character position of the start of the error in the expression string.  
  
 `ppParsedExpression`  
 [out] Returns the parsed expression in an [IDebugParsedExpression](../vs140/IDebugParsedExpression.md) object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method produces a parsed expression, not an actual value. A parsed expression is ready to be evaluated, that is, converted to a value.  
  
## See Also  
 [IDebugExpressionEvaluator](../vs140/IDebugExpressionEvaluator.md)   
 [IDebugParsedExpression](../vs140/IDebugParsedExpression.md)   
 [PARSEFLAGS](../vs140/PARSEFLAGS.md)