# Introduction to Visual Studio Code Debugger

As we suggested you to use VSCode to develop QuiSP, we would like to introduce how you can use VSCode Debugger to debug the unit-tests and the simulation tests.

## Caution

Everytime you start a debug session, you should make sure that you have compiled QuiSP.  
It is a common mistake to start a debug session without compiling your edits.  
Before unit-tests, you need to compile QuiSP with `make run-unit-test MODE=debug`.  
Before simulation tests, you need to compile QuiSP with `make exe MODE=debug`.  

## All you need to know to debug

By default, the configurations for the unit-tests and the simulation tests are done for you already.  
To start the debug session, follow these steps:

1. Select the **Run and Debug** icon in the **Activity Bar** on the side of VSCode.
2. Next to the top left of the window, select either **UnitTests** or **Simulation** and click the green play button.  
3. If you have breakpoints set in the QuiSP files, the debugger will stop at the breakpoints and you will be able to inspect the data at that point.  

If you are unfamiliar with VSCode Debugger and want more detailed info, please refer to [this article](https://code.visualstudio.com/docs/editor/debugging)

## Additional tips on debugging unit-tests

When you debug UnitTests according to the previous section, the debug session will run the entire unit-tests in QuiSP.  
It is also possible to debug one test at a time using the C++ TestMate extension, which is preinstalled in the QuiSP Dev Container.

1. From the **Activity Bar**, select the **Testing** icon. Let's say you want to start the debug session for `Init_IsNotInitiator` of `AppTest` group.  
2. In the **Testing** tab that you just opened, open TestMate C++, run_unit_test, and then AppTest.
3. Under the AppTest, there should be several unit-tests that belong to the `AppTest` group. One of them is the `Init_IsNotInitiator` test.  
4. Its debug session can be started once you hover over `Init_IsNotInitiator` and click the play button **Debug Test**.

In the same way, you can pick other tests and start the debug session.
