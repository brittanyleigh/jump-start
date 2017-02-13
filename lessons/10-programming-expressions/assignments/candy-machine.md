# Assignment: Candy Machine

This challenge is to build a computer candy machine.

You’ve got some money and you want to buy some candy.  So, you go up to the candy machine, put in your money, select your candy, and then pick up your candy and your change.  Sounds fun, huh?

Here are two example runs through the program.

```
Welcome to Ada's Computer Candy Machine!
(All candy provided is virtual.)

How much money do ya got? > $1.00

$1.00, that's all?
Well, lemme tell ya what we got here.

A $0.65 Twix
B $0.50 Chips
C $0.75 Nutter Butter
D $0.65 Peanut Butter Cup
E $0.55 Juicy Fruit Gum

So, What'll ya have? > C

Thanks for purchasing candy through us.
Please take your candy, and your $0.25 change!
```


```
Welcome to Ada’s Computer Candy Machine!
(All candy provided is virtual.)

How much money do ya got? > $0.50

$0.50, that's all?
Well, lemme tell ya what we got here.

A $0.65 Twix
B $0.50 Chips
C $0.75 Nutter Butter
D $0.65 Peanut Butter Cup
E $0.55 Juicy Fruit Gum

So, What'll ya have? > D

You're broke. Take your $0.50 and go elsewhere.
```

## Primary Requirements
- Ask the user how much money they have
  - Assume that the `$` symbol is part of the prompt; the user doesn't have to type it in every time.
- Display all candy options and their costs (even if the user cannot afford the candy -- do you know a candy machine where the food you can't afford magically disappears?)
- Decide whether the user can afford the candy or not
  - If they can't, tell them so
  - If they can, calculate and display their change

Need some help getting started? Remember that you can use `gets` to read a String of input from the user. `gets` returns a string with the Enter character that the user typed, but you usually don’t want that. Ruby has a `chomp` method for Strings that removes that Enter (or "newline") character. So you use the following to get input from without the extra newline at the end and assign it to a variable.

`response = gets.chomp`

Of course you can name that variable whatever makes sense in the context. Remember there are several ways to solve a programming problem, so it is possible to do something completely different and still solve the problem.

## Optional Enhancements
- Handle when the buyer enters "C" or "c" so that it works as expected. DONE
- Do something appropriate when the buyer enters an invalid amount for the money and an invalid selection.

```
puts "Welcome to my Computer Candy Machine!\n"
puts "How much money do you have?"
user_amount = gets.chomp
a= 0.65
b= 0.50
c= 0.75
d= 0.65
e= 0.55
puts "\nAlright, you have $" + user_amount + "."
puts "This is what we have :\n"
puts "A $0.65 Twix
B $0.50 Chips
C $0.75 Nutter Butter
D $0.65 Peanut Butter Cup
E $0.55 Juicy Fruit Gum\n
What would you like??"
user_choice = gets.chomp
#as is, user_choice is a string, following case statments convert user_choice to float
case user_choice
when "a", "A"
  user_choice = a
when "b", "B"
  user_choice = b
when "c", "C"
  user_choice = c
when "d", "D"
  user_choice = d
when "e", "E"
  user_choice = e
else
  puts "That's not an option!"
end


if user_amount.to_f >= user_choice
  #.to_f converts user_amount from string to float
  puts "\nEnjoy your candy! Your change is $" + (user_amount.to_f - user_choice).to_s
  #.to_s converts change calculation to string, so it can be displayed
else
  puts "\nUh oh, you don't have enough money for that!!"
end
```
