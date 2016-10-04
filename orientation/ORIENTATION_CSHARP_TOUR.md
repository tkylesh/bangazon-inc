#CSharp Tour

###What you will learn
You will learn about the the structure of a command line application and look at the code in a simple application that displays message to the console.
###Prerequisites
You will need the .NET Core SDK installed https://www.microsoft.com/net/download or Visual Studio Code installed https://code.visualstudio.com/Download

#Creating a .net core app
  1. Create a directory called "HelloDotNet
  2. Using the command line app of your choice cd to the folder you created for your app
  3. Create a new app: dotnet new
  4. Build the app and restore any get any missing libraries (packages) : dotnet restore
  5. Run the app: dotnet run
  6. You should see the test "Hello World".

  
 #Examine the newly created application
 Navigate to the folder where the app was created 
 You will see the following:
 **project.json**-Contains configuration information
 
 **project.lock.json**-Used during the restore process to make sure no nuget packages are missing
 
 **program.cs**-Class that contains the main method, the starting point when your application is ran.
 
 **bin folder**-Contains the compiled code
 
 **obj folder**-Contain debug info


###Main Method
All command line applications use the Main method as their entry point to an application. 

```
     public static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
        }
```
Arguments can be passed to the Main Method.
Here is an example of a main method that accepts an argument.
In this case we are passing a date. 
```
dotnet run 1/1/2017
```
This is how the passed in date is used by the application. 
```
 public static void Main(string[] args)
        {
            var purchaseDate=args[0];
            Console.WriteLine(CustomerGreeting(purchaseDate).ToString());
        }
```
 
###Program.cs
The Main method is usually found in a c# class called Program. It has an extension of .cs.  As you can see from the example below a CSharp class can contain methods. Notice that the class is using a Name Space. Namespaces serves two purposes:

1. Namespaces are heavily used in C# programming in two ways. First, the .NET Framework uses namespaces to organize its many classes.
2. Second, declaring your own namespaces can help you control the scope of class and method names in larger programming projects. Use the namespace keyword to declare a namespace. Notice the class is contained in a namespace called "ConsoleApplication". The name space can be changed to something more specific. Oftentimes an application will have several names spaces in it. Don't assume that name spaces is related to folder structure, often it is the case but they are not related. 
You can find additional information regarding name spaces here: https://msdn.microsoft.com/en-us/library/0d941h9d.aspx
