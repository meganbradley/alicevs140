---
title: "auto_ptr::reset"
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
ms.topic: article
ms.assetid: a8cb1832-ce90-4613-ac1c-37e74b16e4a1
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_ptr::reset
The member function evaluates the expression **delete myptr**, but only if the stored pointer value **myptr** changes as a result of a function call. It then replaces the stored pointer with **ptr**.  
  
## Syntax  
  
```  
  
      void reset(  
   Type* _Ptr = 0  
);  
```  
  
#### Parameters  
 `_Ptr`  
 The pointer specified to replace the stored pointer **myptr**.  
  
## Example  
  
```  
// auto_ptr_reset.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
class Int   
{  
public:  
   Int( int i )   
   {  
      x = i;  
      cout << "Constructing " << ( void* )this << " Value: " << x << endl;   
   };  
   ~Int( )   
   {  
      cout << "Destructing " << ( void* )this << " Value: " << x << endl;   
   };  
  
   int x;  
};  
  
int main( )   
{  
   auto_ptr<Int> pi ( new Int( 5 ) );  
   pi.reset( new Int( 6 ) );  
   Int* pi2 = pi.get ( );  
   Int* pi3 = pi.release ( );  
   if ( pi2 == pi3 )  
      cout << "pi2 == pi3" << endl;  
   delete pi3;  
}  
```  
  
 **Constructing 00311AF8 Value: 5**  
**Constructing 00311B88 Value: 6**  
**Destructing 00311AF8 Value: 5**  
**pi2 == pi3**  
**Destructing 00311B88 Value: 6**   
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [auto_ptr Class](../vs140/auto_ptr-Class.md)