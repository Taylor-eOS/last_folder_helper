This project provides a small Python utility for remembering the last folder a program used. It is designed to be lightweight, dependency free, and reusable across unrelated projects without forcing them to share state.<br>
The module works by saving the chosen path to a hidden text file in the current working directory. Because the file is local to where the script runs, each project automatically maintains its own independent “last folder” value. No configuration is required.<br>
After installing the package, import it in your script and request the stored folder before prompting the user. When the user selects a new folder, save it so it becomes the default next time.<br>
<b>Import</b> the script like any pip package (in a virtual environment) as: `git+https://github.com/Taylor-eOS/last_folder_helper.git`<br>
Example usage:<br>
```
import last_folder_helper

default = last_folder_helper.get_last_folder()
folder = input(f"Input folder ({default}): ").strip() or default
last_folder_helper.save_last_folder(folder)
```
