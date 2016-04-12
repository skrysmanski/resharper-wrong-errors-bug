Steps to reproduce:

1. Open "ReSharper-WrongErrorsBug.sln"
2. Build solution
3. Enable solution-wide-analysis (note that no errors show up, which is correct)
4. Close Visual Studio
5. Open solution again

Now R# will say that it can't find "SomeCliClass" in "TestClass.cs". However, the solution
will still build fine.

Note also that a rebuild doesn't resolve the wrong error.
