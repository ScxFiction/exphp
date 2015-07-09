# Programmer Interview Scope Scxripts 
	 Section PDO - PHP Data Objects

#### 1. Explain Prepared Statements ?

* Template for SQL query that uses values from user input
* Placeholders for values stored in varibles
	- Can be used for column values
	- Cannot be used for column names or operators
	- Non-numeric values are automatically wrapped in quotes
* Prevents SQL injection
* More efficient when same query is reused
* Can bind results to named varibles


#### 2. Explain Using Prepared Statements ?

* Prepare and validate the SQL with placeholders
* Bind values to the placeholders
* Execute the statement
* Bind output values to varibles (optonal)
* Fetch the results

##### 2.1 Binding Values

 [List of Constants](http://php.net/manual/en/pdo.constants.php)

* Binding values to placeholders
    - Use bindParam() or bindValue()
    - Pass an array of values to the execute() method
* Output values
    - Use bindColumn()
    - Named variables simplify display in web page

#### 3. What is a Transaction ?

* Set of SQL queries executed as a unit
* Operation is committed only if all parts succeed
* Transaction can be rolled back if an error occurs
* Particularly useful for financial transfers
* Prevents rows being modified by another connection


#### 4. Fetching Results

* fetch() gets the next row from a result set
* fetchAll() creates an array containing all rows
* fetchColumn() gets a single column from the next row
* fetchObject() gets the next row as an object

#### 5. PDO vs MySqli

* Benchmark tests inconclusive
* MySqli and PDO access the same underlying driver
* MySqli: WordPress and Jommla!
* PDO:Drupal(WordPress also considering)
* No clear winner
