
# Codecademy COURSE
## Learn PHP
- Learn the fundamentals of PHP, one of the most popular languages of modern web development.
---
### 1. Getting Started with to PHP
#### 1.1 Introduction to PHP
> **1.1.1 History of PHP**

PHP was created in 1994 and is one of the foundational technologies of modern web development. Given all the new technologies used today, is there still a place for PHP?

PHP remains one of the widest used server-side technologies on the internet. It provides the underlying code for many popular content management systems (CMS) including [WordPress](https://wordpress.com/), [Drupal](https://www.drupal.org/), and [Joomla](https://www.joomla.org/). A *CMS* allows users to create and update their own websites without having to write a lot of complex code themselves.

PHP also provides the underlying code for many e-commerce sites including [WooCommerce](https://woocommerce.com/) and [Magento](https://magento.com/). These e-commerce platforms offer a number of tools for selling products online. This way companies can focus on other aspects of their business without having to implement complex programming logic from scratch.

PHP contains built-in functionality for interacting with web data, *Vanilla PHP*, or PHP without any other tools, can be used on its own to create web application back-ends. But we don’t have to reinvent the wheel every time! Once we’re comfortable with the basics of the PHP language, we have our pick of powerful PHP frameworks to choose from! These frameworks provide scaffolding and solutions to common problems in back-end web development. Some popular PHP frameworks are [Laravel](https://laravel.com/), [CakePHP](https://cakephp.org/), and [Symfony](https://symfony.com/).

![PHP_Ecosystem](https://content.codecademy.com/courses/updated_images/PHP_Ecosystem-09-09.svg)

> **1.1.2 How is PHP used in HTML?**

PHP is often used to build *dynamic web pages*. A *dynamic web page* is one where each visitor to the website gets a customized page that can look different than how the site looks to another visitor. This is in contrast to *static web pages* which provide the same content to each visitor.

![php_static_dynamic](https://content.codecademy.com/courses/introduction-to-php/php_static_dynamic.svg)

In order to create this dynamic behavior, PHP was designed to work closely with HTML. PHP can be used directly in-line with an HTML document. When the web site is delivered from the back-end to the front-end, the PHP content is executed and added to the HTML to form one HTML document. The start of in-line PHP is denoted with `<?php` and the end is denoted with `?>`.

As an example, consider the following code:

```php
<p>This HTML will get delivered as is</p>
<?php echo "<p>But this code is interpreted by PHP and turned into HTML</p>";?>
````

In PHP, the `echo` keyword is used to output text. The text in this case is everything between the double quotes (`"`). An instruction written in PHP is called a statement. A semicolon (`;`) is required at the end of each statement in PHP.

So when the code above is executed, it outputs the text into the HTML file and the front-end will receive the following HTML document:

```php
<p>This HTML will get delivered as is</p>
<p>But this code is interpreted by PHP and turned into HTML</p>
```
> *Instructions*
> - We’ve included the example from the narrative here so that you can see it in action. When you are ready, continue to the next exercise.

```php
#index.php
<h1>My First PHP Site</h1>
<p>This HTML will get delivered as is</p>
<?php echo "<p>But this code is interpreted by PHP and turned into HTML</p>";?>
<?php echo "<ul><li>You can use any HTML tags,</li><li>like this list.</li></ul>";?>
<footer>
  <p>And this code is back in plain HTML</p>
</footer>
```
<img width="593" alt="Output" src="https://user-images.githubusercontent.com/104789666/187547019-b59c2055-8fe8-43ea-8d32-a013a57f7b74.png">

> **1.1.3 How is PHP Executed?**

In the previous exercise, we explored how PHP can be sent from the back-end to the front-end where it is received as HTML to be displayed by a browser.

PHP is flexible and can also be executed from the terminal. We can use PHP as a general purpose programming language to write programs that give simple instructions to the computer without involving HTML or the web. When this is done, the output of the program is logged to the terminal. This is useful when testing functionality or for writing simple local programs.

When writing a PHP script file, we still need to denote that we are beginning our PHP code using `<?php`, but the closing tag is no longer required. It is typically left out by convention.

For example, if the following code were placed in **index.php**:

```php
<?php
echo "Hello, World!";
```

When the code above is run, `"Hello, World!"` will be output to the terminal.

Generally, PHP ignores whitespace (tabs, spaces, new lines), so this code yields the same result as the previous example:

```php
<?php
echo     "Hello, World!";
You may be surprised that this code also works:
```

```php
<?php
Echo "Hello, World!";
```

Unlike many other languages, PHP is not always case-sensitive, so `Echo` is a valid statement in PHP. However, it’s best practice to use standard casing – in this case, `echo`.

> *Instructions*
> ```php 
> <?php
> echo "I love PHP!";
> ```
> - We’ve included some sample code - can you change it so that I love PHP! is printed to the terminal instead of Hello, World!?

```php
<?php
echo "Hello, World!";
````
> **1.1.4 PHP Comments**

Sometimes, we want to include text in our files that we don’t want the computer to execute or display to the end user. We can do this with *comments*. Comments can be used to annotate our code to make it clearer to ourselves or others. They are also useful to prevent lines of code from being executed without deleting them.

In PHP, there are two main ways to add comments to our code. The first is single line comments. These are typically used for short explanations or points of clarification. Either `#` or `//` can be used to create a single line comment. Anything on the same line after these symbols is not executed by PHP.

For example:

```php
// I will always remember this
echo "Hello world"; // My first PHP statement
```
or
```php
# I will always remember this
echo "Hello, World!"; # My first PHP statement
```
The second type of comment is a multi-line comment. This is used for longer descriptions, a more detailed guide on how to properly use the section of code, or to prevent several lines of code from being executed. These comments are started with `/*` and ended with `*/`.

For example:

```php
/* "I've never thought of PHP as more 
than a simple tool to solve problems."
- Rasmus Lerdorf */
echo "Hello, World!";
```

> *Instructions*
> - This PHP code includes both single and multi line comments. Take a moment to predict what will show up in the terminal and what will not. When you’re ready run the code to see if you were right.

```php
#index.php
<?php
// I will always remember this
echo "Hello, World!"; # My first PHP statement

/* "I've never thought of PHP as more 
than a simple tool to solve problems."
- Rasmus Lerdorf */
echo "\nRasmus is the creator of PHP!";
```

> **1.1.5 Review**

In the next lesson, you’ll start creating your own PHP code. Take a second and review what you already know about PHP:

- Despite its age, PHP is still a commonly used technology in web development.
- PHP is designed to interact with HTML to generate dynamic websites.
- Embedding PHP in HTML is done by placing PHP code between `<?php` and `?>` tags.
- Every statement in PHP must be terminated with a semicolon `;`.
- PHP files have a **.php** extension and the file always starts with the opening PHP tag `<?php`. The closing tag is implied and left out by convention.
- Whitespace is generally ignored when executing PHP code.
- Keywords are not case sensitive in PHP. As a convention, use the standard casing.
- Single line comments are made in PHP using `#` or `//`. Multi-line comments are placed between `/*` and `*/`.

### 2. Learn PHP Variables
#### 2.1 PHP Strings and Variables
> **2.1.1 Strings**

![php-strings-variables-1](https://content.codecademy.com/courses/php-strings-variables/PHP_m2l1e1.svg)

In everyday conversation, we use the word data to refer to any sort of information. This information is often a list of numbers, like a company’s monthly expenses or statistics about an athlete’s performance. However, in programming, data means something very specific. It’s still information, but that information takes the form of a few specific types.

The PHP language has different ways of handling different types of data. Which actions the computer can perform and how the computer stores the data in memory will vary based on the type. In this lesson, we’ll be learning about the *string* data type.

Strings are words or pieces of text that the computer treats as a single item. A string is a sequence of characters. It can be any length and contain any letters, numbers, symbols, or spaces surrounded by quotation marks.

```php
echo "My first string"; // Prints: My first string
```

It’s important to distinguish between strings and the rest of the code in a PHP program. Every part of a program is text, but strings are the parts we intend to keep as data—not as instructions to be executed by computer. In this lesson we’re going to focus on strings wrapped in double quotation marks (if you’re curious, you can check out [the official PHP documentation](http://php.net/manual/en/language.types.string.php) to see other types of PHP strings).

In later lessons, we’ll be using PHP to create custom HTML documents enabling dynamic web pages. As we learn the basics, however, we’ll be writing simple PHP only programs that run in the terminal.

Let’s make some strings!

> *Instructions*
> - Let’s start with [the classic](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program). Use the `echo` keyword to print `Hello, World!`. <br>
You should always end a PHP statement with a semicolon.

```php
#index.php
<?php
// Write your code below:
  echo "Hello, World!";
```

> **2.1.2 Escape Sequences**

We use quotation marks to indicate the start and end of a string. The quotation marks tell the computer that we want everything inside them to be treated as a single piece of data. But how do we include quotation marks inside a string?

Consider the following string: `"She said "hi" to the dog."`

In the code above, the quotes around “hi” are intended to be part of the string, but the computer will actually see two strings `"She said "` and `" to the dog."` with `hi` in between. Since `hi` won’t be recognized as valid PHP it will result in an error:

```php
echo "She said "hi" to the dog."; //syntax error, unexpected 'hi' (T_STRING)
```

In order to indicate which quotation marks the computer should view as instructions vs which it should view as simply characters, PHP allows for escape sequences. An escape sequence usually consists of a backslash (`\`) immediately followed by another character.

```php
echo "She said \"hi\" to the dog."; // Prints: She said "hi" to the dog.
```

Quotation marks aren’t the only symbol requiring an escape sequence. When we print multiple strings, PHP will print them to the same line by default:

```php
echo "1. Go to gym";
echo "2. Cook dinner"; 
```

The code above will output `1. Go to gym2. Cook dinner.` To print the second string on a new line, we can use the newline escape sequence (`\n`):

```php
echo "1. Go to gym";
echo "\n2. Cook dinner"; 
/* Prints
1. Go to gym
2. Cook dinner
*/
```

You don’t need to worry about other escape sequences yet, but if you’d like to see the full list you can find one in [the PHP documentation](http://php.net/manual/en/language.types.string.php#language.types.string.syntax.double).

Let’s practice!

> *Instructions*
> - Let’s make a to-do list for you. Use `echo` to print a string to the console in the following format: `1. [thing you have to do].` For example, here’s ours: `1. Teach PHP`.

```php
#index.php
<?php
// Write your code below:
echo "1. [thing you have to do]";
```

> *Instructions*
> - Let’s create a new `echo` statement for the next item on our to-do list. <br>
> By default, this second statement would print on the same line as the first… Start this second string with the escape sequence for a new line character. Next, continue the string in the same format as before: `2. [Another thing to do]`.

```php
#index.php
<?php
// Write your code below:
echo "1. [thing you have to do]";
echo "\n2. [Another thing to do]";
```

> *Instructions*
> - Let’s throw a third thing on the list. This time, let’s mix it up. Include something inside your string wrapped in double quotes. For example, here’s ours `3. Learn to have "fun"`.

```php
#index.php
<?php
// Write your code below:
echo "1. [thing you have to do]";
echo "\n2. [Another thing to do]";
echo "\n3. Learn to have \"fun\"";
```

> **2.1.3 String Concatenation**

It can be useful to combine two strings together. This process is called *string concatenation*, and we can use the concatenation operator (`.`) to do this.

An *operator* is a character that performs a task in our code. The computer will take the string to the left of the concatenation operator, combine it with the string to the right, and return the resulting single string. Let’s see an example of string concatenation:

```php
echo "one" . "two"; // Prints: onetwo
```

Notice how the string “onetwo” was printed. The computer won’t make any assumptions for us—it will combine the strings exactly as they are without adding any spaces or line-breaks. If we want spaces, we’ll have to add any spaces we want ourselves. Here we added a space to the string `"one "`:

```php
echo "one " . "two"; // Prints: one two
```

We can also combine, or chain, our operations to get a final result:

```php
echo "one" . " " . "two" . " " . "three"; // Prints: one two three
```

The concatenation operator takes two strings (the *operands*) and produces a string as a result (the return value). As we delve deeper into PHP, we’ll learn about other kinds of operators. Most will take one or two operands, but there’s even one that takes three.

Let’s join some strings together!

> *Instructions*
> - Use `echo` to print the string `"Code"` concatenated to the string `"cademy"`.

```php
#index.php
<?php
// Write your code below:   
echo "Code"."cademy";
```

> *Instructions*
> - We want to learn a little more about you. Uncomment the line of code that starts with `echo "\nMy name is:"` and concatenate the given string with a string containing your name. Include a space after the colon without editing the string we provided.

```php
#index.php
<?php
// Write your code below:   
echo "Code"."cademy";

echo "\nMy name is:" . " " ."Ramazan İlter";
```

> *Instructions*
> - Use `echo` to print a final portmanteau by concatenating these four strings `"\n"`, `"tur"`, `"duck"`, and `"en"`. Make sure to include a semicolon after the statement.

```php
#index.php
<?php
// Write your code below:   
echo "Code"."cademy";

echo "\nMy name is:" . " " ."Ramazan İlter";

echo "\n"."tur"."duck"."en";
```

> **2.1.4 Variables**

![php-strings-and-variables-2](https://content.codecademy.com/courses/php-strings-variables/PHP_m2l1e4m.svg)

Let’s say I have a really long string in my program, and I’m going to need to use it multiple times. Do I have to type the string out every time I need to use it? The answer is “no”. Variables are a fundamental programming concept designed to address this concern. With variables, we store values so that we can easily reuse them throughout a program.

Before we can use variables in our code, we need to declare and assign them.

Declaring a variable is the process of reserving a word, the *variable name*, which we’ll be able to refer to in our code. It’s good practice to name the variable in a way that describes the data it holds.

*Assignment* is the process of associating that variable name with a specific value so that everytime we use the variable’s name the computer will grab that value.

![php-strings-variables-3](https://content.codecademy.com/courses/php-strings-variables/PHP_m2l1e4n.gif)

> **2.1.5 Creating Variables**

Let’s look at an example of creating a variable:

```php
$my_name = "Aisle Nevertell";
```

In the code above, we’re actually doing two things with a single statement: we’re *declaring* a new variable by giving it the name `my_name`. We’re also assigning it the value `"Aisle Nevertell"`. The variable `$my_name` now holds the value `"Aisle Nevertell"`.

To declare a variable we use the dollar sign character (`$`) followed by our chosen variable name. The dollar sign is known as a *sigil*; it’s a character that allows the computer to see quickly that something is a variable.

To assign it a value we use another operator: the assignment operator (`=`) followed by the value we’re assigning to the variable.

Though it can occasionally be useful to separate these actions, we’ll most often be declaring and assigning variables at the same time.

![php-strings-variables-4](https://content.codecademy.com/courses/php-strings-variables/PHP_m2l1e5.svg)

In PHP, variables names can contain numbers, letters, and underscores (`_`), but they have to start with either a letter or an underscore. Variable names are case sensitive, meaning that PHP will treat the variables `$my_example` and `$My_example` as two different variables.

One common convention when naming PHP variables is to use an underscore between words on variable names with more than one word in their name. This is known as *snake case*:

```php
$mood = ":)";
$favorite_food = "Red curry with eggplant";
```

Let’s create some variables!

> *Instructions*
> - Create a variable and assign to it a string value. You can give the variable any valid name you’d like and assign a string containing anything you want. End the statement with a semicolon.

```php
#index.php
<?php
// Write your code below:
  
$silly = "without common sense, absurd, ridiculous";
```

> *Instructions*
> - Declare a variable `$biography` and assign to it a string that starts with a new line character and contains a sentence or two about you.

```php
#index.php
<?php
// Write your code below:
  
$silly = "without common sense, absurd, ridiculous";

$biography="\nMy name is Ramazan. I am learning PHP Software Language";
```

> *Instructions*
> - Create a variable `$favorite_food` and assign to it the string `"\n"`, `"tur"`, `"duck"`, and `"en"` concatenated together.

```php
#index.php
<?php
// Write your code below:
  
$silly = "without common sense, absurd, ridiculous";

$biography="\nMy name is Ramazan. I am learning PHP Software Language";

$favorite_food="\n"."tur"."duck"."en";
```

> **2.1.6 Using Variables**

Once we’ve declared a variable and assigned a value to it, we can use it as many times as we want. We refer to a variable by using the dollar sign followed by the variable’s name.

```php
$favorite_food = "Red curry with eggplant, green beans, and peanuts";
echo $favorite_food; 
// Prints: Red curry with eggplant, green beans, and peanuts
```

Except during assignment, whenever the computer sees a variable in your code, it replaces the variable with the value assigned to that variable.

```php
$dog_name = "Tadpole";
echo $dog_name; 
// Prints: Tadpole
```

Since the computer treats a variable just as if it were the value it holds, this means we can do operations on variables just as we would with any value of that type.

```php
$dog_name = "Tadpole";
echo "My dog is named " . $dog_name; 
// Prints: My dog is named Tadpole
```

In the code above, we concatenated the string `"My dog is named "` to the value held by the `$dog_name` variable (`"Tadpole"`). Let’s look at another example that uses multiple variables:

```php
$dog_name = "Tadpole";
$favorite_food = "salmon";
$color = "brown";
 
echo "I have a " . $color . " dog named " . $dog_name . " and her favorite food is " . $favorite_food . ".";
// Prints: I have a brown dog named Tadpole and her favorite food is salmon.
```

Let’s use some variables!

> *Instructions*
> - You’re going to create a couple variables. The variable, `$name`, should be assigned your name as a string. The second, `$language`, should be assigned a string value representing a language you’re learning.

```php
#index.php
<?php
// Write your code below:
$name = "Ramazan";
$language = "PHP";
```

> *Instructions*
> - Use `echo` to print any string you’d like with the `$name` variable concatenated to it.

```php
#index.php
<?php
// Write your code below:
$name = "Ramazan";
$language = "PHP";
  
echo "Sometimes ".$name." is"." learning ".$language.".";
```

> *Instructions*
> - Use `echo` to print a string starting with a newline (`\n`) with `$language` variable concatenated to it.

```php
#index.php
<?php
// Write your code below:
$name = "Ramazan";
$language = "PHP";
  
echo "Sometimes ".$name." is"." learning ".$language.".";

echo "\nSometimes\n".$name."\nis"."\nlearning\n".$language."\n.";
```

> **2.1.7 Variable Parsing**

In the last exercise, we saw how concatenating a number of strings and string variables got annoying. There’s an easier way!

PHP strings allow us to place variables directly into double quoted strings. These variables will be *parsed* which means the computer will read the variables as the value they hold rather than see them as just a sequence of characters.

```php
$dog_name = "Tadpole";
$favorite_food = "salmon";
$color = "brown";

echo "I have a $color dog named $dog_name and her favorite food is $favorite_food.";
// Prints: I have a brown dog named Tadpole and her favorite food is salmon.
```

PHP string parsing is incredibly useful. Whenever PHP sees a dollar sign (`$`) inside a string it will assume all the characters next to it (until it reaches a character that couldn’t be included in a variable name) are a part of the variable name.

Sometimes this can get complicated. Consider the following example:

```php
$toy = "frisbee";
echo "Alex likes playing with $toys";
```

The code above will cause an error. Why? The computer was looking for a variable `$toys` and couldn’t find one.

Fear not! PHP allows us to specifically indicate the variable name by wrapping it in curly braces to avoid any confusion. We’ll include the dollar sign followed by the variable name wrapped in curly braces:

```php
$dog_name = "Tadpole";
$favorite_food = "treat";
$color = "brown";
 
echo "I have a ${color}ish dog named $dog_name and her favorite food is ${favorite_food}s.";
// Prints: I have a brownish dog named Tadpole and her favorite food is treats.
```

Let’s have PHP do some variable parsing for us!

> *Instructions*
> ```php
> #index.php
> <?php
> // Fill in the blanks in the code below:
>   $noun = "___";
>   $adjective = "___";
>   $verb = "___";
> ```
> - We’re going to write a silly sentence PHP program. There are a number of variables assigned the string ‘___’. Replace each of them with words of the designated type.

```php
#index.php
<?php
// Fill in the blanks in the code below:
  $noun = "helicopter";
  $adjective = "powerful";
  $verb = "scream";
```

> *Instructions*
> ```php
> #index.php
> <?php
>   echo "The world's most beloved ___ was very ___ and loved to ___ every single day.";
> ```
> - Beneath the three variables, there’s an `echo` statement with three blanks (___) in it. Replace those blanks with the three variables (in the order they were declared).

```php
#index.php
<?php
// Fill in the blanks in the code below:
  $noun = "helicopter";
  $adjective = "powerful";
  $verb = "scream";

  echo "The world's most beloved $noun was very $adjective and loved to $verb every single day.";
```

> *Instructions*
> ```php
> #index.php
> <?php  
>   //Fix the code below and uncomment it:
> 
>  // echo "\nI have always been obsessed with > $nouns. I'm $adjectiveish. I'm always > $verbing.";
> ```
> - At the end of the program, there’s a commented out line of code. We commented it out because it wasn’t working properly. Fix the line of code and uncomment it.

```php
#index.php
<?php
// Fill in the blanks in the code below:
  $noun = "helicopter";
  $adjective = "powerful";
  $verb = "scream";

  echo "The world's most beloved $noun was very $adjective and loved to $verb every single day.";


//Fix the code below and uncomment it:

 echo "\nI have always been obsessed with ${noun}s. I'm ${adjective}ish. I'm always ${verb}ing.";
```

> **2.1.8 Variable Reassignment**

The word variable comes from the latin variāre which means “to make changeable.” This is an apt name because the value assigned to a variable can change.

![php-strings-variables-5](https://content.codecademy.com/courses/php-strings-variables/PHPVariable_m2l1e8.gif)

The process of assigning a new value to a variable is called *reassignment*. We reassign a variable using the assignment operator on a variable that’s already been declared:

```php
$favorite_food = "Red curry with eggplant";
echo $favorite_food; // Prints: Red curry with eggplant
 
// Reassign the value of $favorite_food to a new string
$favorite_food = "Pizza"; 
echo $favorite_food; // Prints: Pizza
```

It’s often useful to create new variables assigned to the same value as an existing variable:

```php
$first_player_rank = "Beginner";
$second_player_rank = $first_player_rank;
```

In the code above, we declared the variable `$first_player_rank` and assigned to it the string `"Beginner"`. Next, we declared `$second_player_rank` and assigned it to `$first_player_rank`.

This created a new variable (`$second_player_rank`) assigned the value `"Beginner"`. Notice how variables can be treated different depending on where they appear in code. During variable assignment or reassignment, the variable on the left of the assignment operator is treated as a variable (named storage for holding a value) while a variable on the right of the operator is treated as the value it stores. 

> *Instructions*
> ```php
> #index.php
> <?php
>   $movie = "___";
> // Add your code here:
> 
> 
> 
>   echo "I'm a fickle person, my favorite movie > used to be $movie.";
> ```
> - We declared a variable `$movie` and assigned the string `"___"` to it. But that’s no fun! Beneath that declaration, reassign `$movie` so that it’s assigned a string containing your favorite movie from when you were a little kid.

```php
#index.php
<?php
  $movie = "___";
// Add your code here:
  $movie = "Transformers";

  echo "I'm a fickle person, my favorite movie used to be $movie.";
```

> *Instructions*
> ```php
> #index.php
> <?php
>   $movie = "___";
> // Add your code here:
>   $movie = "Transformers";
> 
>   echo "I'm a fickle person, my favorite movie > used to be $movie.";
> ```
> - Below your reassignment of the `$movie` variable, declare and assign a new variable, `$old_favorite`. The `$old_favorite` variable should have `$movie` assigned to it.

```php
#index.php
<?php
  $movie = "___";
// Add your code here:
  $movie = "Transformers";
  $old_favorite = $movie;

  echo "I'm a fickle person, my favorite movie used to be $movie.";
```

> *Instructions*
> ```php
> #index.php
> <?php
>   $movie = "___";
> // Add your code here:
>   $movie = "Transformers";
>   $old_favorite = $movie;
> 
>   echo "I'm a fickle person, my favorite movie > used to be $movie.";
>   
> // Add a statement here:
> 
>   
>   echo "\nBut now my favorite is $movie.";
>   
> // Add a statement below:
> ```
> - Between the first and second `echo` statements, reassign the value of `$movie` to a new string.

```php
#index.php
<?php
  $movie = "___";
// Add your code here:
  $movie = "Transformers";
  $old_favorite = $movie;

  echo "I'm a fickle person, my favorite movie used to be $movie.";
  
// Add a statement here:
  $movie = "Godfather";
  
  echo "\nBut now my favorite is $movie.";
  
// Add a statement below:
```

> *Instructions*
> ```php
> #index.php
> <?php
>   $movie = "___";
> // Add your code here:
>   $movie = "Transformers";
>   $old_favorite = $movie;
> 
>   echo "I'm a fickle person, my favorite movie > used to be $movie.";
>   
> // Add a statement here:
>   $movie = "Godfather";
>   
>   echo "\nBut now my favorite is $movie.";
>   
> // Add a statement below:
> ```
> - Finally, at the end of the program add one last `echo` statement which uses PHP string parsing to print a string containing the `$old_favorite` variable.

```php
#index.php
<?php
  $movie = "___";
// Add your code here:
  $movie = "Transformers";
  $old_favorite = $movie;

  echo "I'm a fickle person, my favorite movie used to be $movie.";
  
// Add a statement here:
  $movie = "Godfather";
  
  echo "\nBut now my favorite is $movie.";
  
// Add a statement below:
  echo "\nBut I'll always have a special place in my heart for $old_favorite.";
```

> **2.1.9 Concatenating Assignment Operator**

We can assign and reassign variables to the values that result from operations:

```php
$full_name = "Aisle" . " Nevertell";
echo $full_name; // Prints: Aisle Nevertell
```

During assignment, the computer will first evaluate everything to the right of the assignment operator and return a single value.

In the code above, the computer will concatenate the strings `"Aisle"` and `" Nevertell"` into the value `"Aisle Nevertell"`. It will then assign this string as the value to the `$full_name` variable.

This is true even for more complex operations:

```php
$full_name = "Aisle" . " " . "Nevertell" . " " . "Nomaderwat";
echo $full_name; // Prints: Aisle Nevertell Nomaderwat
```

One theme you may notice as you learn a programming language’s syntax is that common actions that programmers need to do a lot often have a shortcut. Consider the following:

```php
$full_name = "Aisle";
$full_name = $full_name . " Nevertell";
echo $full_name; // Prints: Aisle Nevertell
```

In the code above, we have the variable `$full_name` assigned the value `"Aisle"`. We want to reassign `$full_name` to its current value appended with the string `" Nevertell"`.

Believe it or not, this is such a common task that PHP offers a shorthand notation, the concatenating assignment operator (`.=`). Let’s compare the same action but using this alternate operator:

```php
$full_name = "Aisle";
$full_name .= " Nevertell";
echo $full_name; // Prints: Aisle Nevertell
```

It may seem funny to provide a shortcut to save just a few characters of typing, but when operations are performed often enough, those keystrokes can really add up. This syntax is also faster and easier to read which makes code easier to maintain.

One important thing to note is that even though PHP is often flexible about whitespace, it is inflexible with the concatenating assignment operator—the `.` and `=` characters must not have any spaces or other whitespace characters between them.

Let’s practice!

> *Instructions*
> ```php
> #index.php
> <?php
>   echo "I'm going on a picnic!";
> 
>   $sentence = "\nI'm going on a picnic, and I'm taking apples";
> 
>   echo $sentence;
> 
> // Write your code below:
> ```
> - We’re going on a picnic. We started you off with the `$sentence` variable holding the value `"\nI'm going on a picnic, and I'm taking apples"`.<br>
Use the concatenating assignment operator (`.=`) to add another item to our list. The string you append should start with a comma(`,`) and a space followed by a word which starts with the letter “b”.<br>
Next use `echo` to print the new value of `$sentence`.

```php
#index.php
<?php
  echo "I'm going on a picnic!";

  $sentence = "\nI'm going on a picnic, and I'm taking apples";

  echo $sentence;

// Write your code below:
  $sentence .= ", b";
  echo $sentence;
```

> *Instructions*
> ```php
> #index.php
> <?php
>   echo "I'm going on a picnic!";
> 
>   $sentence = "\nI'm going on a picnic, and I'm taking apples";
> 
>   echo $sentence;
> 
> // Write your code below:
>   $sentence .= ", b";
>   echo $sentence;
> ```
> - That was fun. Let’s keep playing.<br>
This time use the concatenating assignment operator (`.=`) to append a string which starts with a comma(,) and a space followed by a word which starts with the letter “c”.<br>
Use `echo` to print the newest value of `$sentence`.

```php
#index.php
<?php
  echo "I'm going on a picnic!";

  $sentence = "\nI'm going on a picnic, and I'm taking apples";

  echo $sentence;

// Write your code below:
  $sentence .= ", b";
  echo $sentence;

  $sentence .= ", c";
  echo $sentence;
```

> **2.1.10 Assign by Reference**

When we create a variable assigned to another variable, the computer finds a new space in memory which it associates with the left operand, and it stores a copy of the right operand’s value there.

![php-strings-variables-6](https://content.codecademy.com/courses/php-strings-variables/PHPVariable_4_v3.gif)

This new variable holds a *copy* of the value held by the original variable, but it’s an independent entity; changes made to either variable won’t affect the other:

```php
$first_player_rank = "Beginner"; 
$second_player_rank = $first_player_rank; 
echo $second_player_rank; // Prints: Beginner
 
$first_player_rank = "Intermediate"; // Reassign the value of $first_player_rank
echo $second_player_rank; // Still Prints: Beginner
```

We can also create an alias, or nickname, for a variable. Instead of a copy of the original variable’s value, we create a new name which points to the same spot in memory.

![php-strings-variables-7](https://content.codecademy.com/courses/php-strings-variables/PHPVariable_5_v3.gif)

We use a different operator for this—the reference assignment operator (`=&`).

When we *assign by reference* we’re saying that the variable on the left of the operator should point, or *refer*, to the exact same data as the variable on the right. With assignment by reference, changes made to one variable will affect the other:

```php
$first_player_rank = "Beginner";
$second_player_rank =& $first_player_rank; 
echo $second_player_rank; // Prints: Beginner
 
$first_player_rank = "Intermediate"; // Reassign the value of $first_player_rank
echo $second_player_rank; // Prints: Intermediate
```

Ok, let’s get some practice!

> *Instructions*
> ```php
> #index.php
> <?php
> /* Imagine a lot of code here */  
>   $very_bad_unclear_name = "15 chicken wings";
> 
> // Write your code here:
> ```
> - You’ve inherited some code from another developer. You can’t change their code, but you need to add some additional functionality. Instead of using the `$very_bad_unclear_name` variable as is in your part of the code. Declare a new variable, `$order`, as a reference to the `$very_bad_unclear_name` variable.

```php
#index.php
<?php
/* Imagine a lot of code here */  
  $very_bad_unclear_name = "15 chicken wings";

// Write your code here:
  $order =& $very_bad_unclear_name;
```

> *Instructions*
> ```php
> #index.php
> <?php
> /* Imagine a lot of code here */  
>   $very_bad_unclear_name = "15 chicken wings";
> 
> // Write your code here:
>   $order =& $very_bad_unclear_name;
> 
> 
> 
> 
>   
>   // Don't change the line below
>   echo "\nYour order is: $very_bad_unclear_name.";
> ```
> - Use the concatenation assignment operator to append more things to `$order`.<br>
Awesome! Notice how when we `echo` the `$very_bad_unclear_name` variable at the end of the programs, the changes you made are reflected in the output!

```php
#index.php
<?php
/* Imagine a lot of code here */  
  $very_bad_unclear_name = "15 chicken wings";

// Write your code here:
  $order =& $very_bad_unclear_name; 

  $order .= ", 1 cheeseburger";

  $order .= ", 3 side salads";
    
  // Don't change the line below
  echo "\nYour order is: $very_bad_unclear_name.";
```

> **2.1.11 Review**

Awesome work! We’ve covered a lot of material in this lesson, so let’s review:

- Strings are collections of text that the computer treats as a single piece of data.
- A string can be any length and contain any letters, numbers, symbols, or spaces surrounded by quotation marks.
- In order to include certain characters inside strings we have to use escape sequences.
- An *operator* is a character that performs a task in our code.
- We can use the concatenation operator (`.`) to combine two strings into one.
- Variables are a fundamental programming concept which allow us to easily reuse data in our code.
- We declare a variable using the dollar sign (`$`) followed by the variable name and then use the assignment operator (`=`) to give it a value.
- PHP has variable parsing which allows us to include variables directly in our strings.
- Once a variable has been assigned, we can change its value. This is called reassignment.
- We can create an alias for a variable, instead of just a copy, using the reference assignment operator (`=&`).
- Operations to the right of the assignment operator will be evaluated before assignment takes place.
- The concatenating assignment operator (`.=`) is a shorthand notation for reassigning a string variable to its current value appended with another string value.

If that was a lot to take in, don’t worry about memorizing everything right away. Remember that when you want to explore more about the language, [the documentation](http://php.net/manual/en/langref.php) is a great place to get comfortable exploring.

```php
#index.php
<?php

  echo "Hello, Learner!";
  
  echo "\nWe hope you enjoyed this lesson.";
  
  echo "\nAre you excited?" . "\nTo learn more?";
  
  $favorite_language = "PHP";
  
  $message = "$favorite_language is by far our favorite language.";
  
  $message .= " It's yours now too, right?";
  
  echo "\n" . $message . " Right?!";  
````

```
#Output

Hello, Learner!
We hope you enjoyed this lesson.
Are you excited?
To learn more?
PHP is by far our favorite language. It's yours now too, right? Right?!
```

#### 2.2 PHP Numbers
> **2.2.1 Numbers**


## ***(To be continued...)***
---
