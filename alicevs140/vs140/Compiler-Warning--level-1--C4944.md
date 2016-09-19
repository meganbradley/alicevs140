---
title: "Compiler Warning (level 1) C4944"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e2905eb1-2e3b-4fab-a48b-c0cae0fd997f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4944
'symbol' : cannot import symbol from 'assembly1': as 'symbol' already exists in the current scope  
  
 A symbol was defined in a source code file and then a #using statement referenced an assembly that also defined the symbol. The symbol in the assembly is ignored.  
  
## Example  
 The following sample creates a component with a type called ClassA.  
  
```  
// C4944.cs  
// compile with: /target:library  
// C# source code to create a dll  
public class ClassA {  
   public int i;  
}  
```  
  
## Example  
 The following samples generate C4944.  
  
```  
// C4944b.cpp  
// compile with: /clr /W1  
class ClassA {  
public:  
   int u;  
};  
  
#using "C4944.dll"   // C4944 ClassA also defined C4944.dll  
  
int main() {  
   ClassA * x = new ClassA();  
   x->u = 9;  
   System::Console::WriteLine(x->u);  
}  
```