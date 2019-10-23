# Lab 11: PHP Includes
*Due: Thursday, October 24, 2019*

For this lab, you will take your existing website from your lab assignments and factor out some of the duplicate code, and place the duplicate code in *Server-Side Includes* using PHP.

## Step 1: Setup

- Make a copy of your lab09 folder and name the new folder **lab11** (skip "lab10")

*Note: this lab assumes you've been following along with the instructions correctly and you have a **start.html** file <u>and</u> your other HTML files in your **lab09** folder*

## Step 2: Change the files from HTML to PHP

- Change the file extensions of all the HTML files from **.html** to **.php**

Reminder: after you change the file extensions you can no longer view your web pages by simply double-clicking on the HTML files. From here on out you need to work in your "web root" and view your files on your "localhost"

## Step 3: Setup the new "include" files

- Inside the **lab11** folder create a new folder named **inc**
- In the **inc** folder create two new plain text files with these names:<br>**html-top.php**<br>**nav.php**
- Open all the **.php** files (the files that used to be .html) in your code editor
- Also open the two new **.php** files from the **inc** folder in your code editor

The rest of this lab requires you to juggle a lot of open files while copying and pasting code between them. It's easy to make mistakes and mess thing up. Go slowly!

## Step 4: Replace the header HTML with a PHP Include

- Pick any one of your **.php** files EXCEPT the **start.php** file.  *Copy* the following code to your computer's clipboard...

```html
<!doctype html>
<html lang="en">
<head>
	<meta charset="utf-8">
	<title>Lab 9 – Shakespeare</title>
	<link rel="stylesheet" href="css/styles.css">  
	<link rel="stylesheet" href="css/navigation.css">
</head>
```

...and paste it into the file: **html-top.php**

*(Don't use your start.php file because it doesn't have the link to the "navigation.css" file!)*

- [ ] Edit the code in the **html-top.php** file – update the lab number: "**Lab 9 - ...**" to "**Lab 11 - ...**"
- [ ] In ALL five PHP files (that's the four webpages, plus start.php) replace the top part (the doctype down to the closing HEAD tag) and insert a PHP Include statement that points to the **html-top.php** file 

*Refer to your notes from the last lecture regarding the syntax you need to use for the "PHP Include" statement. to point to html-top.php*

## Step 5: Replace the menu HTML with a PHP "include"

Note: doing this step will break the "is-current" menu highlighter. That's okay. We'll fix it in a later lab assignment.

- [ ] In any of your **.php** files except the **start.php** file, *copy* the following code to your computer's clipboard...

```html
<nav class="menu">
	<ul>
		<li><a class="is-current" href="cats.html">Cats</a></li>
		<li><a href="dogs.html">Dogs</a></li>
		<li><a href="fish.html">Fish</a></li>
		<li><a href="bears.html">Bears</a></li>
	</ul>
</nav>
```

...and paste it into the file: **nav.php**

*(Don't use your start.php file because it doesn't have a NAV element!)*

- [ ] Edit the code in the **nav.php** file: 
  - Replace every instance of **.html** with **.php**
  - Remove the `class="is-current"`
- [ ] In ALL five PHP files replace the entire NAV element with a PHP Include statement that points to the **nav.php** file 
- [ ] Although the *start.html* file didn't have a NAV element, go ahead and **add the PHP Include for the nav.php file** between the HEADER and the SECTION (with the class="lead").  We'll need it there for the future labs.

## Step 6: Upload your Work

When you are done with your webpage, close everything and use an FTP tool to access your account on **csc170.org** and upload your files:

- In a web browser (any), go to this address to check your handiwork:<br> **www.csc170.org/accountname/lab11/start.php**<br>(where "*accountname*" is your account name)

## Step 7: Report your work

- In our Blackboard section, in Lab 11, post a link to your webpage to receive credit for this Lab.