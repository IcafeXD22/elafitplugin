<p align="center">
  <a href="https://elaf.it">
    <img alt="elafhotel" src="https://elaf.it/images/logo.png">
  </a>
</p>

<p align="center">
  ELAF Hotel Plugin API.
</p>

<p align="center">
  <a href="#links"><img alt="Backers on Open Collective" src="https://img.shields.io/badge/links-1-brightgreen.svg"></a>
  <a href="#features"><img alt="Sponsors on Open Collective" src="https://img.shields.io/badge/features-7-brightgreen.svg"></a>
  <a href="#plugin-functions"><img alt="Sponsors on Open Collective" src="https://img.shields.io/badge/SQL Functions-1-brightgreen.svg"</a>
  <a href="#allowed-tables-with-example"><img alt="Sponsors on Open Collective" src="https://img.shields.io/badge/Allowed Tables-1-brightgreen.svg">

# Links

- [Hotel](https://elaf.it)

# Features

- [Hello World]
- [UserID]
- [Protect]
- [Credits]
- [Diamonds]
- [Item]
- [SQLInsert]

# Sample
```
<?php
	require(__DIR__.'/includes.php');
?>

<h1>Hello World!</h1>
<p>
    <img src="/images/Elaf_friends.png" alt="" class="align-right">
</p>
<p>Sag der Welt Hallo!:</p>
<p><?= $Plugin->helloWorld(); ?></p>
```

# Plugin Functions
| Function   	| Description                    	| Use                                                                                     	| Returns              	|
|------------	|--------------------------------	|-----------------------------------------------------------------------------------------	|----------------------	|
| HelloWorld 	| Returns Echo for Testing       	| $Plugin->helloWorld();                                                                  	| echo                 	|
| UserID     	| Returns User ID as INT         	| $Plugin->getUserID();                                                                   	| int                  	|
| Protect    	| Protect String for SQL or POST 	| $Plugin->Protect(string) (string "string to Protect")                                   	| string               	|
| Credits    	| Give or Take Credits           	| $Plugin->Credits(string, int) (string "give, take")                                     	|                      	|
| Diamonds   	| Give or Take Diamonds          	| $Plugin->Diamonds(string, int) (string "give, take")                                    	|                      	|
| Item       	| Give Item                      	| $Plugin->Item(int) (int "ItemID")                                                       	|                      	|
| SQLInsert  	| Insert into allowed SQL Tables 	| $Plugin->SQLInsert(string, array) (string "allowed Table", array "see under SQL Guide") 	| false if not allowed 	|


# SQL Functions
## Insert
	Sample:
		$Plugin->SQLInsert('AllowedTable', array('column' => 'value', 'column2' => 'value2'));



# Allowed Tables (with Example)
## CMS_NEWS
### Table
| id   	| title  	| short_story 	| long_story 	| author 	| timestamp 	| image  	| published        	| room             	| views            	|
|------	|--------	|-------------	|------------	|--------	|-----------	|--------	|------------------	|------------------	|------------------	|
| Auto 	| String 	| String      	| Text       	| String 	| Timestamp 	| String 	| int (Default: 1) 	| int (Default: 0) 	| int (Default: 0) 	|
### Sample
$Plugin->SQLInsert('cms_news', array('title'	=>	'TEST', 'short_story' => 'ABC', 'long_story' => 'lang', 'author' => 'JOJO', 'timestamp' => time(), 'image' => 'abc.png'));
