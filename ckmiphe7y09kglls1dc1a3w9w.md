## Convert .py file to .exe file

**Steps:**

1.Go to [python.org](https://python.org) and  install  it on your device

2.Go to the folder where you have the .py file

3.Shift + right-click and open PowerShell window

4. Type `pip install pyinstaller`.

since I have already installed it on my device it's showing the requirement already satisfied.

5. Now run the command `pyinstaller -w yourfilename.py`

This will create a directory including all library packages.

Go to the **dist** folder you will find your .exe file with additional files and packages.

6.To get rid of all additional files and pack them into a single .exe file.

run the command `pyinstaller -w -F yourfilename.py`.

Note: if your .py files run in the console and don't have any GUI 

run command `pyinstaller  -F yourfilename.py`

Done 

Open the **dist** folder again you will find a .exe file and you can directly execute it.

Video Tutorial: [https://www.youtube.com/watch?v=uSVFoC1pqAI](https://www.youtube.com/watch?v=uSVFoC1pqAI)