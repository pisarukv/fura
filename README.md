# Fura
Fura is CLI tool for analysing git repositories.

 - **Portable** : Fura is a perfect cross-platform tool. Single binary, no dependencies.  Just run and it works
 - **Perfect for experiments** 🔬: Perfect match with other languages. Integrate Fura to your script or notebook. Use it to create something great.


# Installation
Just download binary for your OS and its ready to work. 

# Known issues 
On Windows progress bar is displayed incorect. Use `-noprogress` to disable it. 

# Examples
To launch the binary all you need to do is write `./fura` (for macos or linux) or `fura` (for Windows).
![alt text](https://github.com/cali4888/fura/blob/master/process_view.jpg)

 You can either put binary file to the folder with repository either pass the `-repo` param with path of repo. 
![alt text](https://github.com/cali4888/fura/blob/master/start_repo_remote.jpg)

After finishing running data will be saved to json with the name of repository. 
![alt text](https://github.com/cali4888/fura/blob/master/process_finished.jpg)

![alt text](https://github.com/cali4888/fura/blob/master/json_saved.jpg)

You can pass `-output` param to change the output file name. 
For more info about params look [wiki page](https://github.com/cali4888/fura/wiki/Params-list)
