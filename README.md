# sqlpdo

Console access to database by PHP PDO

Following example:
```
./sqlpdo

Connections
test  Environ test
test2 Environ test 2

select one of the links above: test
SQL>create table a (id int);

SQL>insert into a (id) values (1);
Affected rows: 1
Timing: 0.003312

SQL>select * from a;
+--+
|id|
+--+
| 1|
+--+
Rows: 1
Timing: 0.000808
```

## Configuring connections

Edit sqlpdo.xml

Example of 2 connetions using the driver sqlite:
```xml
<?xml version="1.0"?>
<pdo history=".sqlpdo.hst" history_size="50" verbose="true">
	<dsn id="test" user="" passwd="" dsn="sqlite:/tmp/teste.db">Environ test</dsn>
	<dsn id="test2" user="" passwd="" dsn="sqlite:/tmp/teste2.db">Environ test 2</dsn>
</pdo>
```

Configure one or more &lt;dsn&gt; [driver PDO](http://br1.php.net/manual/en/pdo.drivers.php) used.

## License

(The MIT License)

Copyright (c) 2013 Edison E. Abreu [&lt;dinho.abreu@gmail.com&gt;](mailto://dinho.abreu@gmail.com)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
