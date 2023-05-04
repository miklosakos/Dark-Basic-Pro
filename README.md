# How to compile tutoriale becase Lee fucked it up like a totally professional software developer :)

You need to install [Visual Studio 2010](https://archive.org/details/en_vs_2010_ult) and [Visual Studio 2010 SP1](https://archive.org/details/vs-2010-sp-1dvd-1), [Microsoft DirectX SDK August 2007](https://archive.org/details/dxsdk_aug2007), [Visual Studio 2012](https://archive.org/details/en_visual_studio_professional_2012_x86_dvd)

Open the solution file exclusively in VS 2012 and do not let it update project files, leave them as is!
Now, locate the GameFX project, right click it, click on properties, open up Linker and click general. Change the output file to: `$(ProjectDir)\..\..\..\..\Install\Compiler\plugins\DBProGameFX.dll` then click OK. I have no clue if that's the right place but at least compiles.

Now do the same with Objects and change the output file to: `$(ProjectDir)\..\..\..\..\Install\Compiler\plugins\DBProBasic3DDebug.dll`, again, I have no clue if that's the right location for the compiled file.

Repeat the same steps for the Transport project and change the output file to: `$(ProjectDir)\..\..\..\..\Install\Compiler\plugins\DBPro($TargetName)Debug.dll`, I have no idea still if that's the right directory where the linked DLL should go but at least it compiles. :)

Now right click on Solution 'Dark Basic Pro' and choose Build. Depending on your machine this can take a while. :)

# Dark-Basic-Pro
Dark Basic Pro is an open source BASIC programming language for creating Windows applications and games. The solution requires Microsoft DirectX SDK (August 2007).

Over the years, Dark Basic Pro produced many first and third party plugins which we have made free thanks to permission from third party developers.

[DarkPHYSICS V1](http://fstore.thegamecreators.com/DarkBasicPro/DarkPhysics_v1.zip) & 
[DarkPHYSICS Update 105](http://fstore.thegamecreators.com/DarkBasicPro/DarkPhysics_Update_105.zip)

Notes:

1. The Synergy Editor assumes DBPro is directly installed in the default folder for 32-bit program files on the OS drive: "C:\Program Files (x86)\Dark-Basic-Pro\". To change this behavior open the file "Editor\Synergy Editor.cfg" and change the value of the "DBPLocation" property accordingly. The value of the "DBPLocation" property in the 090216 and 120216 binary releases has a placeholder value used on development that most likely will need to be changed.

2. The default folder destination assumed by plug-in installers might differ from the actual folder where the installation sits on. When prompted by an installer to choose a different destination do it accordingly.
