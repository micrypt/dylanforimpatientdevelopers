#Diving in head first

Enough fooling around.  It is time to dive into writing some real dylan code, and at the end of this chapter, actually having something useful.  That something useful will be an application that takes a JSON file and converts it to an Objective-C model that will parse the JSON (actually an NSDictionary)

##Building a JSON to Objective-C model generator

###Creating a project
Create a project using make-dylan-app called json-to-objc in the same way we created a hello world app in Chapter 001.  After creating the project, open json-to-objc.dylan

###Getting the filename
We can grab the filename from the command line arguments.  To do this we will use the 'arguments' vector (basically an array in any other language).  We will check if arguments have been provided, and if so, we will start out by printint out that file name.  If not, we will show an error.

we can do this by adding the following snippet to json-to-objc.dylan:

```dylan
if(arguments.size == 0)
  format-out("please provide a source file\n");
else
  let filename = arguments[0];
  format-out(filename);
end;
```

_notice:_ We have learned in the last statement how to check a vectors size, how to print to the terminal, and access specific elements of a vector.

###A better error handler
 
###File IO
###JSON parsing
###Generating the output

####JSON to NS type mapping