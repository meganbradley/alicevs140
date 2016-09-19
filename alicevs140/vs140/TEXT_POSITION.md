---
title: "TEXT_POSITION"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6dcec574-a852-49fa-8c2e-2e71cbb5e3c6
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# TEXT_POSITION
Describes the line and column location in the given text.  
  
## Syntax  
  
```cpp#  
typedef struct _tagTEXT_POSITION {   
   DWORD dwLine;  
   DWORD dwColumn;  
} TEXT_POSITION;  
```  
  
```c#  
public struct TEXT_POSITION {   
   public uint dwLine;  
   public uint dwColumn;  
};  
```  
  
## Members  
 dwLine  
 Index of line in source file.  
  
 dwColumn  
 Character offset into line.  
  
## Remarks  
 This structure is used in the [CONTEXT_INFO](../vs140/CONTEXT_INFO.md) and [DisassemblyData](../vs140/DisassemblyData.md) structures.  
  
 This structure is filled in by a call to the following methods:  
  
-   [IDebugDocumentContext2::GetStatementRange](../vs140/IDebugDocumentContext2--GetStatementRange.md)  
  
-   [IDebugDocumentContext2::GetSourceRange](../vs140/IDebugDocumentContext2--GetSourceRange.md)  
  
-   [IDebugDocumentPosition2::GetRange](../vs140/IDebugDocumentPosition2--GetRange.md)  
  
-   [IDebugFunctionPosition2::GetOffset](../vs140/IDebugFunctionPosition2--GetOffset.md)  
  
 This structure is passed as a parameter to the following methods:  
  
-   [IDebugDocumentText2::GetText](../vs140/IDebugDocumentText2--GetText.md)  
  
-   [IDebugDocumentTextEvents2::OnInsertText](../vs140/IDebugDocumentTextEvents2--onInsertText.md)  
  
-   [IDebugDocumentTextEvents2::OnRemoveText](../vs140/IDebugDocumentTextEvents2--onRemoveText.md)  
  
-   [IDebugDocumentTextEvents2::OnReplaceText](../vs140/IDebugDocumentTextEvents2--onReplaceText.md)  
  
-   [IDebugDocumentTextEvents2::OnUpdateTextAttributes](../vs140/IDebugDocumentTextEvents2--onUpdateTextAttributes.md)  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [IDebugDocumentContext2::GetStatementRange](../vs140/IDebugDocumentContext2--GetStatementRange.md)   
 [IDebugDocumentContext2::GetSourceRange](../vs140/IDebugDocumentContext2--GetSourceRange.md)   
 [GetRange](../vs140/IDebugDocumentPosition2--GetRange.md)   
 [GetOffset](../vs140/IDebugFunctionPosition2--GetOffset.md)   
 [GetText](../vs140/IDebugDocumentText2--GetText.md)   
 [IDebugDocumentTextEvents2](../Topic/IDebugDocumentTextEvents2.md)   
 [CONTEXT_INFO](../vs140/CONTEXT_INFO.md)   
 [DisassemblyData](../vs140/DisassemblyData.md)