# Fura 🚛
Fura is CLI tool for analysing git repositories.

 - **Portable** : Fura is a perfect cross-platform tool. Single binary, no dependencies.  Just run and it works
 - **Perfect for experiments** 🔬: Perfect match with other languages. Integrate Fura to your script or notebook. Use it to create something great. Chek our [wiki](https://github.com/cali4888/fura/wiki/Data-format) for data format.

# Installation
Just download binary for your OS and put it in folder with repo or other place from which you will start it.

# Examples
To use the binary file you must launch terminal and launch it by writing `./fura` (for macos or linux) or `fura` (for Windows). In Windows it can be launched without entering the terminal. You can either put binary file to the folder with repository either pass the `--repo` (`-r`) param with path of repo. 
![alt text](https://github.com/cali4888/fura/blob/master/images/scan_start.png)

After finishing running data will be saved to json with the name of repository. 

![alt text](https://github.com/cali4888/fura/blob/master/images/json_saved.png)

You can pass `-output` param to change the output file name. 
For more info about params look [wiki page](https://github.com/cali4888/fura/wiki/Params-list)

# Known issues 
On Windows progress bar is displayed incorect. Use `-noprogress` to disable it. 
