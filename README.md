# Subnautica Always Day Patch
This is a guide to enable always day in Subnautica by patching a game file.

**NOTE:** You do NOT need to be tech savvy to do this, all you need is the ability to follow instructions.

[![Video Guide](https://img.youtube.com/vi/leixcZaJcsI/maxresdefault.jpg)](https://youtu.be/leixcZaJcsI)

## Prerequisites
[dnSpy](https://github.com/dnSpy/dnSpy/releases) - dnSpy is a widely known Open Source program that is used for viewing/editing .NET assemblies, this may look complicated but it's pretty easy to get a grasp of.

## Guide
First thing you need to do is go to the Subnautica's game files, if you don't know how [here](https://i.imgur.com/QVlYGMy.png) is an example.

Now from the game directory navigate to ``Subnautica_Data`` and then ``Managed``, once in the ``Managed`` folder look for ``Assembly-CSharp.dll``, it should be the very first file in the list if you sort by name alphabetically (default sorting method in windows).

Now you need to drag and drop the ``Assembly-CSharp.dll`` file on to the Assembly Explore in dnSpy, [here](https://i.imgur.com/N8PEro8.gif) is an example.

Once ``Assembly-CSharp.dll`` is loaded into dnSpy press ``Ctrl + Shift + K``, this should open up a Search box below, in the search box type ``GetDayScalar`` in the search box.

![](https://i.imgur.com/7EAMTgR.png)

Now you're going to want to double click on the ``GetDayScalar`` that is in orange text, it should bring you to something that looks like this:

![](https://i.imgur.com/ZnKC3Yr.png)

Right click the highlighted ``GetDayScalar()`` text and click on ``Edit Method (C#)...``, once the window pops up replace the code on **line 13** with ``return 0.45f;`` like this:

![](https://i.imgur.com/aiZZhpo.png)

once you're done click the ``Compile`` button in the bottom right and once the window closes click the exit button on the top right.

![](https://i.imgur.com/FGLCCtN.png)

When this window opens click ``Yes``, after that another window will pop up and all you have to do is click ``OK``.

![](https://i.imgur.com/XzOq66A.png)

Bam you're done if you ever want to undo the patch you can verify integrity of game files in steam or save the old code somewhere and repatch it if you want, verifying integrity of game files is easier for newbies though, if you don't know how you can just google it.

## Q&A
Q. Why go through all this work to just set it to always be day?
  - Like most people here we just want a casual gaming experience without having to deal with the pain of night time.

Q. Can't I just do this with some cheat code?
  - The only way would be to type a time command in console every time night came which would get repetitive and annoying, this would also skip time which causes issues with the story since it has automatic triggers based on time (i.e. aurora explosion), with what I provided we are only editing the skybox and not the actual time.
  
Q. Why not just provide the patched game file, it would be easier?
  - Not sure how the Game Developers would feel about me posting it, it is technically their work and it requires a licenses to own, so posting it here would allow people without a game license to aquire a part of the game.
  
## Reporting Issues
If you have any issues you can make a issue ticket on github or contact me @``Cloaker#7584`` on Discord.
