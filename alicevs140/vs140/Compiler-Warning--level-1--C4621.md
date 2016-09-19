---
title: "Compiler Warning (level 1) C4621"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 40931bd9-cb89-497e-86f0-cec9f016c63c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4621
no postfix form of 'operator --' found for type 'type', using prefix form  
  
 There was no postfix decrement operator defined for the given type. The compiler used the overloaded prefix operator.  
  
 This warning can be avoided by defining a postfix `--` operator. Create a two-argument version of the `--` operator as shown below:  
  
```  
// C4621.cpp  
// compile with: /W1  
class A  
{  
public:  
   A(int nData) : m_nData(nData)  
   {  
   }  
  
   A operator--()  
   {  
      m_nData -= 1;  
      return *this;  
   }  
  
   // A operator--(int)  
   // {  
   //    A tmp = *this;  
   //    m_nData -= 1;  
   //    return tmp;  
   // }  
  
private:  
   int m_nData;  
};  
  
int main()  
{  
   A a(10);  
   --a;  
   a--;   // C4621  
}  
```