# Section-Logic-SQL
 PL/pgSQL code block that declares a variable lvLetter with the value of 'M', then checks if it is one of the allowed characters in the IF statement. If lvLetter is not one of the allowed characters, it raises an exception with the message '$'.

If lvLetter is one of the allowed characters, it then checks which range it falls into using a series of IF statements. Each range has a corresponding notice statement that prints a number to the console. If lvLetter does not fall into any of the allowed ranges, it raises an exception with the message '$'.

If any exceptions are raised, the exception message is caught by the EXCEPTION block and printed to the console.
