# File Sorter
Streamlining the process of organizing your files easier on your Windows machine, A very minimal design interface that accompanies you without needing much explanation.

## Setup Instructions
- Added the functionality to call it through command-line
- You can set it up either through:
```
python "Path/To/PythonFile" "Path/To/Directory/To/Be/Sorted"
eg. python "C:/Users/test/FileSorter/fileSort.py" "C:/Users/test/Downloads"
```
- Or alternatively, with a slight setup process, you can run "FileSort" in any powershell terminal and it'll sort the CWD.

## Setup for FileSort PWSH Function
- 1. Open Powershell, type the command `notepad $PROFILE`
- 2. Add a function to the profile:
```
function fileSort {
    $cwd = Get-Location
    python "Path/To/PyFile" $cwd # Change Path/To/PyFile with location where the python file is saved.
}
```
- 3. After the setup, you can open powershell in any folder and run the command "FileSort" with which, it's going to sort all the files in the working directory


## How It Works

- It works with the simple principle of organizing files in a given folder with it's filetypes.
- The `fileExtensions.py` consists a map with each file type to a certain folder name.
- The main program looks for all singular scattered files in a given desktop location, ignoring all folders.
- And it proceeds to create folders for each depending on the map of the file extensions.
- Assuming the program has permission to move items in the given location, it will proceed to move the files to their designated folder.

## Author(s)

- [Hemanth Tenneti](https://github.com/HemanthTenneti)

## Disclaimers, if any
This program can only run on Windows machines as it uses the dialog picker of the Windows Operating System. However, if the code were to be edited to suit your needs, I would assume it can work with other OS'es or UNIX systems aswell with slight changes.
