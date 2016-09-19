---
title: "Boxing Nullable Types (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bdb5b626-abc0-405d-8f64-0f0a0bf883a4
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Boxing Nullable Types (C# Programming Guide)
Objects based on nullable types are only boxed if the object is non-null. If <xref:System.Nullable`1.HasValue?qualifyHint=False> is `false`, the object reference is assigned to `null` instead of boxing. For example:  
  
```  
bool? b = null;  
object o = b;  
// Now o is null.  
```  
  
 If the object is non-null -- if <xref:System.Nullable`1.HasValue?qualifyHint=False> is `true` -- then boxing occurs, but only the underlying type that the nullable object is based on is boxed. Boxing a non-null nullable value type boxes the value type itself, not the <xref:System.Nullable`1?qualifyHint=True> that wraps the value type. For example:  
  
```  
bool? b = false;  
int? i = 44;  
object bBoxed = b; // bBoxed contains a boxed bool.  
object iBoxed = i; // iBoxed contains a boxed int.  
```  
  
 The two boxed objects are identical to those created by boxing non-nullable types. And, just like non-nullable boxed types, they can be unboxed into nullable types, as in the following example:  
  
```  
bool? b2 = (bool?)bBoxed;  
int? i2 = (int?)iBoxed;  
```  
  
## Remarks  
 The behavior of nullable types when boxed provides two advantages:  
  
1.  Nullable objects and their boxed counterpart can be tested for null:  
  
    ```  
    bool? b = null;  
    object boxedB = b;  
    if (b == null)  
    {  
      // True.  
    }  
    if (boxedB == null)  
    {  
      // Also true.  
    }  
    ```  
  
2.  Boxed nullable types fully support the functionality of the underlying type:  
  
    ```  
    double? d = 44.4;  
    object iBoxed = d;  
    // Access IConvertible interface implemented by double.  
    IConvertible ic = (IConvertible)iBoxed;  
    int i = ic.ToInt32(null);  
    string str = ic.ToString();  
    ```  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Nullable Types (C# Programming Guide)](../Topic/Nullable%20Types%20\(C%23%20Programming%20Guide\).md)   
 [How To: Identify a Nullable Type (C# Programming Guide)](../Topic/How%20to:%20Identify%20a%20Nullable%20Type%20\(C%23%20Programming%20Guide\).md)