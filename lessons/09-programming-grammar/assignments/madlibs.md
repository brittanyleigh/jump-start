# Assignment: MadLibs
You are going to create a MadLib game! Use [this resource](https://www.eduplace.com/tales/) if you haven’t played a MadLib in a while to get reacquainted with this thrilling adventure using parts of speech.

## Primary Requirements
- Create a MadLib program that accepts input from the user and outputs a completed MadLib
- Use up to ten different parts of speech in order to fill in your MadLib
- Output should consist of a paragraph of output that has the user’s input substituted into the MadLib

## Example Output
Below is an example output from running through a MadLib exercise. Don’t forget, your code and MadLib should be unique to you!
```
Welcome to my MadLib program. Please enter in some information below:

name: Starr
adjective: huge
noun: tablecloth
adjective: dry
food (plural): tacos
noun (plural): packs
verb ending in -ed: ended
noun: jellyfish

HERE'S YOUR MADLIB.......

Come on over to Starr’s Pizza Parlor where you can enjoy your favorite huge-dish pizza`s.
You can try our famous tablecloth-lovers pizza,
or select from our list of dry toppings,
including delicious tacos, packs, and many more.
Our crusts are hand-ended and basted in jellyfish to make
them seem more Hand-made.
```

## Optional Enhancements
- Use comments to explain your code
- Reuse at least one word
- Ask for at least 1 number
- Explore Ruby's built in methods for [String](http://ruby-doc.org/core-2.2.0/String.html) like `capitalize`, `downcase`, `upcase`, and utilize them accordingly

```
puts "Welcome to MadLibs!"
puts "Fill out each field below, pressing enter after each one."
puts "Country: "
country_one = gets.chomp
puts "Girl's Name: "
girl_name = gets.chomp
puts "A kind of animal: "
animal_one = gets.chomp
puts "An animal name: "
animal_one_name = gets.chomp
puts "Another type of animal: "
animal_two = gets.chomp
puts "Another animal name: "
animal_two_name = gets.chomp
puts "A second country: "
country_two = gets.chomp
puts "A method of transportation (singular noun): "
method_of_transportation = gets.chomp
puts "Plural noun: "
objects = gets.chomp
puts "Plural fruit: "
fruit = gets.chomp
puts "Plural insects: "
insects = gets.chomp
puts "Large Number: "
large_number = gets.chomp

puts "\nHurray, here's your story of adventure!!\n"
#\n at beginning & end create empty new lines before and after this line, so that there is some visual space between entries and story
puts "In a far off part of " + country_one.capitalize + ", lived a girl named " + girl_name.capitalize + ". "
puts "She had a big " + animal_one + " named " + animal_one_name.capitalize + " and a little " +
animal_two + " named " + animal_two_name.capitalize + "."
puts "Everyday, they dreamed of adventure."
puts "So one day they all decided to travel from " + country_one.capitalize + " to " + country_two.capitalize + "."
puts "They fixed up an old " + method_of_transportation + " and set off on their journey."
puts "They saw many great things, like the world's biggest pile of " + objects + "."
puts "They ate many strange foods, like garlic " + fruit + " with salted " + insects + "."
puts "They even visited a land where everything was backwards, and the girl's name became " + girl_name.reverse.capitalize + "."
puts "But after traveling " + large_number + " miles, they got very homesick."
puts "They returned to " + country_one.capitalize + " with new eyes, and a new appreciation for home."

#each line starts with puts so that it displays as new lines, instead of as a paragraph. easier to read!

```
