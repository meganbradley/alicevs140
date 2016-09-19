---
title: "Step 4: Add the CheckTheAnswer() Method"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c66f3831-b4a0-40bc-a109-8f46f4db35ed
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Step 4: Add the CheckTheAnswer() Method
In the fourth part of this tutorial, you'll write a method, `CheckTheAnswer()`, that determines whether the answers to the math problems are correct. This topic is part of a tutorial series about basic coding concepts. For an overview of the tutorial, see [Tutorial 2: Create a Timed Math Quiz](../vs140/Tutorial-2--Create-a-Timed-Math-Quiz.md).  
  
> [!NOTE]
>  If you're following along in Visual Basic, you'll use the `Function` keyword instead of the usual `Sub` keyword because this method returns a value. It's really that simple: a sub doesn't return a value, but a function does.  
  
### To verify whether the answers are correct  
  
1.  Add the `CheckTheAnswer()` method.  
  
     When this method is called, it adds the values of addend1 and addend2 and compares the result to the value in the sum `NumericUpDown` control. If the values are equal, the method returns a value of `true`. Otherwise, the method returns a value of `false`. Your code should look like the following.  
  
     [!CODE [VbExpressTutorial3Step4#8](../CodeSnippet/VS_Snippets_VBCSharp/vbexpresstutorial3step4#8)]  
  
     Next, you'll check the answer by updating the code in the method for the timer's Tick event handler to call the new `CheckTheAnswer()` method.  
  
2.  Add the following code to the `if else` statement.  
  
     [!CODE [VbExpressTutorial3Step4#10](../CodeSnippet/VS_Snippets_VBCSharp/vbexpresstutorial3step4#10)]  
  
     If the answer is correct, `CheckTheAnswer()` returns `true`. The event handler stops the timer, shows a congratulatory message, and then makes the **Start** button available again. Otherwise, the quiz continues.  
  
3.  Save your program, run it, start a quiz, and provide a correct answer to the addition problem.  
  
    > [!NOTE]
    >  When you enter your answer, you must either select the default value before you start to enter your answer, or you must delete the zero manually. You'll correct this behavior later in this tutorial.  
  
     When you provide a correct answer, a message box opens, the **Start** button becomes available, and the timer stops.  
  
### To continue or review  
  
-   To go to the next tutorial step, see [Step 5: Add Click and Enter Event Handlers for the NumericUpDown Control](../vs140/Step-5--Add-Enter-Event-Handlers-for-the-NumericUpDown-Controls.md).  
  
-   To return to the previous tutorial step, see [Step 3: Add a Countdown Timer](../vs140/Step-3--Add-a-Countdown-Timer.md).