# SA:MP Construction (Map Editor)

An independent fork of samp-map-editor by JernejL and vsergeenko777. The fork and significant changes were made by Blefonix Metaverse.

## English (Russian is below)

How to Build:
1. Download and install **[Borland Delphi 7](https://dl.vsergeenko.com/Delphi7.iso)**.
2. Download and compile the components (see below)
3. Download the repository:
```
git clone https://github.com/blefonix/bmsa-editor.git
```
4. In Borland Delphi 7 select **Component -> Install Component**, the **Install Component** window will open
5. In the **Info existing package** tab click **Browse** near **Unit file name** and select all files from **samp-map-editor/components** folder
6. Leave the rest of the fields by default and click OK, confirm rebuilding the package and close the message about successful installation of components
7. Close the project (File -> Close All) without saving it.
8. Open **samp-map-editor/editor.dpr** project through Borland Delphi 7
9. Press **Ctrl+F9** (or Project -> Compile editor), the compilation should complete successfully
10. The executable file **editor.exe** will appear in the project folder, add a DLL (GTAINTERFACE.dll and newton.dll) to it and try to run
### Components
Download the necessary components:
* [GLScene 1.0.0.0714](https://sourceforge.net/projects/glscene/files/GLScene/GLScene%20v1.0.0.0714/glscene_v_1000714_delphi7_full.7z/download)
* [SynEdit 2.1.0](https://github.com/SynEdit/SynEdit/archive/SynEdit-2.1.0-beta.zip)

Compiling GLScene:
1. Extract the files from the **GLScene_v100** folder in the archive to any location, for example **C:\GLScene**.
2. Open project **C:\GLScene\Delphi7\Delphi7.bpg** with Borland Delphi 7, ignore errors about .res files
3. open **Enviroment Options (Tools -> Enviroment Options)**, go to the **Library** tab
4. Press **"... "** button next to **Library path**.
5. Add all GLScene source paths one by one using **"... "** to select folder and **Add** button to add path, you should end up with this list:
```
C:\GLScene\Source
C:\GLScene\Source\Base
C:GLScene\Source\CgShaders
C:GLScene\Source\DesignTime
C:GLScene\Source\FileFormats
C:GLScene\Source\GameAPIs
C:GLScene\Source\PhysicsAPIs
C:GLScene\Source\Platform
C:GLScene/SourcePlugIn
C:GLScene\Source\ScriptingAPIs
C:GLScene\Source\Shaders
C:GLScene/Source/SoundAPIs
C:GLScene\Source\VideoAPIs
```
6. In the **Project Manager** window (it should appear after you open the project), select **GLScene7.bpl**, click **Activate**.
7. Click **GLScene7.bpl** and click **Build**.
8. Probably you will get error **File not found: 'Info.res'**, open **Info.pas** file and remove **{$R Info.res}** line, press **Build** again.
9. If the compilation succeeds, press **Install** in the same menu (click on GLScene7.bpl)
10. You can close the project, saving or not saving - it makes no difference

Compiling SynEdit:
1. Unpack the files from **SynEdit-SynEdit-2.1.0-beta** folder in the archive to any place, for example **C:\SynEdit**
2. Open project **C:\SynEdit\Packages\D7\SynEdit_R7.dpk** (**R7** exactly) through Borland Delphi 7, ignore the error about .res file
3. In the **Package - SynEdit_R7.dpk** window, click Compile
4. It is possible that an error about unexpected symbols in **SynHighlighterJava.pas** file will appear during the compilation, remove them (at the beginning of the file, before the curly braces) and try to compile again
5. If the compilation succeeds, close the project
6. Open the project **C:\SynEdit\Packages\D7\SynEdit_D7.dpk** (exactly **D7**), ignore the error about .res file again
7. In **Package - SynEdit_D7.dpk** window, press Compile, after successful compilation press Install
8. Open **Enviroment Options** again (as in the instruction above), go to **Library**, open **Library path** and add path **C:\SynEdit\Source**.
9. You can close the project by saving or not saving - it makes no difference.

## Russian (English is below)

Инструкция по сборке:
1. Скачайте и установите **[Borland Delphi 7](https://dl.vsergeenko.com/Delphi7.iso)**
2. Скачайте и скомпилируйте компоненты (см. ниже)
3. Склонируйте репозиторий:
```
git clone https://github.com/blefonix/bmsa-editor.git
```
4. В Borland Delphi 7 выберите **Component -> Install Component**, откроется окно **Install Component**
5. Во вкладке **Info existing package** нажмите **Browse** около **Unit file name** и выберите все файлы из папки **samp-map-editor/components**
6. Оставьте остальные поля по умолчанию и нажмите OK, подтвердите пересборку пакета и закройте сообщение про успешную установку компонентов
7. Закройте проект (File -> Close All), не сохраняя его
8. Откройте проект **samp-map-editor/editor.dpr** через Borland Delphi 7
9. Нажмите **Ctrl+F9** (или Project -> Compile editor), компиляция должна завершиться успешно
10. В папке проекта появится исполняемый файл **editor.exe**, дополните его DLL (GTAINTERFACE.dll и newton.dll) и попробуйте запустить
### Компоненты
Скачайте необходимые компоненты:
* [GLScene 1.0.0.0714](https://sourceforge.net/projects/glscene/files/GLScene/GLScene%20v1.0.0.0714/glscene_v_1000714_delphi7_full.7z/download)
* [SynEdit 2.1.0](https://github.com/SynEdit/SynEdit/archive/SynEdit-2.1.0-beta.zip)

Компиляция GLScene:
1. Распакуйте файлы из папки **GLScene_v100** в архиве в любое место, например в **C:\GLScene**
2. Откройте проект **C:\GLScene\Delphi7\Delphi7.bpg** через Borland Delphi 7, проигнорируйте ошибки про .res файлы
3. Откройте **Enviroment Options (Tools -> Enviroment Options)**, перейдите во вкладку **Library**
4. Нажмите кнопку **"..."** напротив **Library path**
5. По очереди добавьте все пути к исходникам GLScene, используя **"..."**, чтобы выбрать папку и кнопку **Add**, чтобы добавить путь, по итогу должен быть такой список:
```
C:\GLScene\Source
C:\GLScene\Source\Base
C:\GLScene\Source\CgShaders
C:\GLScene\Source\DesignTime
C:\GLScene\Source\FileFormats
C:\GLScene\Source\GameAPIs
C:\GLScene\Source\PhysicsAPIs
C:\GLScene\Source\Platform
C:\GLScene\Source\PlugIn
C:\GLScene\Source\ScriptingAPIs
C:\GLScene\Source\Shaders
C:\GLScene\Source\SoundAPIs
C:\GLScene\Source\VideoAPIs
```
6. В окне **Project Manager** (должно было появиться после открытия проекта), выберите **GLScene7.bpl**, нажмите **Activate**
7. Кликните ПКМ по **GLScene7.bpl** и нажмите **Build**
8. Возможно, при компиляции появится ошибка **File not found: 'Info.res'**, откройте файл **Info.pas** и удалите строку **{$R Info.res}**, снова нажмите **Build**
9. Если компиляция завершилась успешно, нажмите **Install** в том же меню (ПКМ по GLScene7.bpl)
10. Проект можно закрыть, сохраняя или не сохраняя - без разницы

Компиляция SynEdit:
1. Распакуйте файлы из папки **SynEdit-SynEdit-2.1.0-beta** в архиве в любое место, например в **C:\SynEdit**
2. Откройте проект **C:\SynEdit\Packages\D7\SynEdit_R7.dpk** (именно **R7**) через Borland Delphi 7, проигнорируйте ошибку про .res файл
3. В окне **Package - SynEdit_R7.dpk** нажмите Compile
4. Возможно, при компиляции появится ошибка про неожиданные символы в файле **SynHighlighterJava.pas**, удалите их (в начале файла, до фигурной скобки) и попробуйте скомпилировать ещё раз
5. Если компиляция завершилась успешно, закройте проект
6. Откройте проект **C:\SynEdit\Packages\D7\SynEdit_D7.dpk** (именно **D7**), снова проигнорируйте ошибку про .res файл
7. В окне **Package - SynEdit_D7.dpk** нажмите Compile, после успешной компиляции нажмите Install
8. Снова откройте **Enviroment Options** (как в инструкции выше), перейдите в **Library**, откройте **Library path** и добавьте путь **C:\SynEdit\Source**
9. Проект можно закрыть, сохраняя или не сохраняя - без разницы.
