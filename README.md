# Fura
Fura is CLI tool for analysing git repositories.

 - **Portable** : Fura is a perfect cross-platform tool. Single binary, no dependencies.  Just run and it works
 - **Perfect for experiments** 🔬: Perfect match with other languages. Integrate Fura to your script or notebook. Use it to create something great.


# Installation
Just download binary for your OS and its ready to work. 

# Running
To run the binary just put it into folder with git repository that you want to scan or pass path to repo through `-repo` param

![alt text](https://github.com/cali4888/fura/blob/master/process_view.jpg)

# Known issues 
On Windows progress is displayed incorect. Use `-noprogress` to disable it. 

# Examples
After getting json data you can use it to calculate diffecent metrics. For example a basic python scrpit for calculating total number of commits,added lines,removed lines.

```python
with open('react.json') as data_file:    
    data = json.load(data_file)

total_commits = 0
added_lines = 0
removed_lines = 0

for day in data['days']:
    for commiter in day['commiters']:#itterating through commiters that made commits on that day
        total_commits =  total_commits + commiter['commits_num']
        added_lines = added_lines + commiter['added_lines']
        removed_lines = removed_lines + commiter['removed_lines']
```
