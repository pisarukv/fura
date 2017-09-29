# Fura 🚛
Fura is CLI tool for analysing git repositories.

 - **Portable** 👣: Fura is a perfect cross-platform tool. Single binary, no dependencies.  Just run and it works
 - **Perfect for experiments** 🔬: Perfect match with other languages. Integrate Fura to your script or notebook. Use it to create something great. 

# Installation
Just download binary for your OS and put it in folder with repo or other place from which you will start it.
Binaries are available for [MacOC 64 bit](https://github.com/cali4888/fura/blob/master/fura-darwin-amd64) , [Windows 64bit](https://github.com/cali4888/fura/blob/master/fura-windows-amd64.exe) , [Linux 64bit](https://github.com/cali4888/fura/blob/master/fura-linux-amd64)


# Examples
To use the binary file you must launch terminal and launch it by writing `./fura` (for macos or linux) or `fura` (for Windows). In Windows it can be launched without entering the terminal. You can either put binary file to the folder with repository either pass the `-r` param with path of repo. 
![alt text](https://github.com/cali4888/fura/blob/master/images/scan_start.png)

After finishing running data will be saved to json with the name of repository. 

![alt text](https://github.com/cali4888/fura/blob/master/images/json_saved.png)

You can pass `-output` param to change the output file name. 
For more info about params look [wiki page](https://github.com/cali4888/fura/wiki/Params-list)

The resulting data is in json format. Check our [wiki](https://github.com/cali4888/fura/wiki/Data-format) for more info about the data format. After this you can use jupyter notebook and write your code for writing different statistics. 

For example you can use this code from [examples page](https://github.com/cali4888/fura/blob/master/examples/basic.md) to calculate total number of commits,added and removed lines for repo. 
For example using this basic script on react repo you will get result ![alt text](https://github.com/cali4888/fura/blob/master/images/basic_example.png)

# Known issues 
On Windows progress bar is displayed incorect. Use `-noprogress` to disable it. 
Do not hesitate to report any bugs that you could find. 
