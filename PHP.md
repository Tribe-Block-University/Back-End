# Tribe Block PHP Tutorial 🐘

PHP is a widely used server-side scripting language designed for web development.

## 📚 Topics Covered
1. [Introduction to PHP](#introduction-to-php)
2. [Setting Up PHP](#setting-up-php)
3. [PHP Syntax & Variables](#php-syntax--variables)
4. [Control Structures](#control-structures)
5. [Functions](#functions)
6. [Handling Forms](#handling-forms)
7. [Working with Databases](#working-with-databases)
8. [Sessions & Cookies](#sessions--cookies)

---

## 1. Introduction to PHP  
PHP (Hypertext Preprocessor) is a scripting language embedded in HTML.
```php
<?php
echo "Hello, PHP!";
?>
```

# Setting Up PHP
* Install XAMPP or MAMP for local development.
* Verify installation with:
```sh
php -v
```

# PHP Syntax & Variables
```php
$name = "John";
$age = 30;
echo "Name: $name, Age: $age";
```

# Control Structures
```php
if ($age > 18) {
    echo "Adult";
} else {
    echo "Minor";
}
```

# Functions
```php
function greet($name) {
    return "Hello, $name!";
}
echo greet("John");
```

# Handling Forms
```php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $username = $_POST["username"];
    echo "Welcome, " . $username;
}
?>
<form method="post">
    <input type="text" name="username">
    <button type="submit">Submit</button>
</form>
```

# Working with Databases
```php
$conn = new mysqli("localhost", "root", "", "mydb");
$sql = "SELECT * FROM users";
$result = $conn->query($sql);
```

# Sessions & Cookies
```php
session_start();
$_SESSION["username"] = "JohnDoe";
echo $_SESSION["username"];
```

🌐 Further Reading
* [PHP Manual](https://www.php.net/manual/en/)
* [W3Schools PHP](https://www.w3schools.com/php/)



