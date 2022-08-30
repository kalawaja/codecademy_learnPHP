
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
> 1. We’ve included some sample code - can you change it so that I love PHP! is printed to the terminal instead of Hello, World!?

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
> 1. This PHP code includes both single and multi line comments. Take a moment to predict what will show up in the terminal and what will not. When you’re ready run the code to see if you were right.

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
