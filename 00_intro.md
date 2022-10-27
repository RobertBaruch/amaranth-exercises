# What's this?

This is a series of graded exercises in using [Amaranth HDL](https://amaranth-lang.org/docs/amaranth/latest/intro.html), the Python-based Hardware Design Language, to design and verify digital circuits!

It's also a work in progress.

Please note, the goal is not to be pedantically correct in every explanation. As you progress through the exercises, you'll learn for yourself the breadth of Amaranth and what you can do with it!

## Prerequisite knowledge

You will need knowledge of:

* Basic digital electronics (do you know what an AND gate is? A flip-flop?)
* Basic Python 3 (do you know how to write a class?)
* How to run things on the command-line (do you know how to use command-line options? What a PATH is?)

## Software prerequisites

YosysHQ has put together a [comprehensive installer](https://github.com/YosysHQ/oss-cad-suite-build#installation) containing everything you need, and then some. Simply follow the instructions.

### Tip for Windows users

If you just downloaded the exe file, it will be in your Downloads folder. Run the executable, and it extracts everything to Downloads/oss-cad-suite. You can simply move the oss-cad-suite directory to somewhere more convient.

*Do not use PowerShell*. Use Command Prompt instead. Always be sure to run `<your-directory>\oss-cad-suite\environment.bat` in Command Prompt before doing any work. You'll know if the environment was set properly if you see `[OSS CAD Suite]` before your prompt:

```txt
F:\amaranth-exercises>..\oss-cad-suite\environment.bat

[OSS CAD Suite] F:\amaranth-exercises>
```

## Tip for vscode users

Open File > Preferences > Settings, look for pylint args, and add:

```txt
--contextmanager-decorators=contextlib.contextmanager,amaranth.hdl.dsl._guardedcontextmanager
```

This is because pylint doesn't recognize that `amaranth.hdl.dsl._guardedcontextmanager` is a valid context manager. Otherwise pylint will complain for every `with m.If` statement.
