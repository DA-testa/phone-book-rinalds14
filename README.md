# Problem:  Phone  book
## Problem Intro duction
In  this  problem  you  will  implement  a  simple  phone  book  manager.

### Problem Description
**Task.** In this task your goal is to implement a simple phone book manager. It should b e able to pro cess thefollowing  typ es  of  user’s  queries:∙

   + **Add** number  name. It means that the user adds a person with name name and phone number number to the phone book. If there exists a user with such numb er already, then your manager has  to  overwrite  the  corresponding  name.∙
    
   + **Del** number.  It  means  that  the  manager  should  erase  a  person  with  number numberfrom  the  phoneb o ok.  If  there  is  no  such  person,  then  it  should  just  ignore  the  query.∙
    
   + **Find** number. It means that the user looks for a person with phone number number. The manager should reply with the appropriate name, or with string “not found" (without quotes) if there is no  such  person  in  the  book.
    
**Input  Format.** There  is  a  single  integer N in  the  first  line  —  the  number  of  queries.  It’s  followed  by N lines,  each  of  them  contains  one  query  in  the  format  described  above.

**Constraints.** 1≤N≤10<sup>5</sup>. All phone numbers consist of decimal digits, they don’t have leading zeros, and each  of  them  has  no  more  than 7 digits.  All  names  are  non-empty  strings  of  latin  letters,  and  each  of them  has  length  at  most 15.  It’s  guaranteed  that  there  is  no  person  with  name  “not  found". 

**Output  Format.** Print the result of each find query — the name corresponding to the phone number or “not found" (without quotes) if there is no person in the phone book with such phone number. Output one  result  per  line  in  the  same  order  as  the find queries  are  given  in  the  input.

**Given file** is a naïve implementation, as self control, complete this task using a fast data structure with better algoritm. Given tests are for self control and give 0 points. Additionaly don't forget to clean input from autotesting additional symbols.

Inputs should contain one enter symbol, not two. Same for output.
## Sample 1.
### Input:
12

add  911  police

add  76213  Mom

add  17239  Bob

find  76213

find  910

find  911

del  910

del  911

find  911

find  76213

add  76213  daddy

find  76213

### Output:
Mom

not found

police

not found

Mom

daddy

### Explanation:
76213 is Mom’s number, 910 is not a number in the phone book, 911 is the number of police, but then it was deleted from the phone book, so the second search for 911 returned “not found". Also, note that when the daddy was added with the same phone number 76213 as Mom’s phone number, the contact’s name  was  rewritten,  and  now  search  for 76213 returns  “daddy"  instead  of  “Mom.

## Sample 2:
### Input:
8

find 3839442

add 123456 me

add 0 granny

find 0

find 123456

del 0

del 0

find 0

### Output:
not found

granny

me

not found

### Explanation:
Recall that deleting a number that doesn’t exist in the phone book doesn’t change anything.
