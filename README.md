##Data Structures and algorithms


###Explanation :

    while((token=getchar())!='n')

Accepts Expression Character by Character Till Entered Character is ‘n’
After Accepting Single Character do all actions inside while loop.

    if(isalnum(token))
    printf("%c",token);

    isalnum(token)   checks whether entered Character is Alphabetic or Numeric .
If Entered Character is alpha-numeric then Directly Display it – for more help [Algo] + [Example]
If Entered Character is Opening Bracket then Push Element Onto Stack

    if(token == '(')
     push(&s,'(');

   If Entered Character is ‘Closing Bracket’ then Pop All Elements till Equivalent Opening Bracket is poped.

    if(token == ')')
      while((x=pop(&s))!='(')
      printf("%c",x);

If Entered Character is Operator then – do

    else
    {
        while(priority(token)< =priority(top(&s)) && !empty(&s))
        {
          x=pop(&s);
         printf("%c",x);
        }
        push(&s,token);
    }
