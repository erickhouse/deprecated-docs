Postman

Use `nextRequest` to control the sequence of postman event that are run after the test completes

You can add shared functions / logic to the collection or folder scope. There is a panel to place logic that gets run on every request within that folder / collection. You can then set a variable `pm.environment.set(keyName)` with is the name of the funciton. The script that wants to use that function calls `eval(keyName)` to load that function into its scope after getting the key from the environment. 

There is a library that will check the schema of the json produces call t4
