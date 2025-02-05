# Galaxy
## Galaxy Classification Project

### Setting up to run the model on Google Colab 
- Download dataset to google drive. Specifically, “MyDrive/data”. Keep the files zipped to save space on your dive (and because our code unzips the files as necessary)
	- Alternatively, download the zip files to a folder of your choice and change the path in the code
	  ``zip_files_path = '/content/drive/MyDrive/YOUR_PATH_HERE/'`` to the path that contains the dataset
- You can either run each code block individually or go to the top of Google Colab and select Runtime->Run all (ctrl+F9).
- In the beginning it will ask to connect to your google drive, so don't walk away right a way.
- Once that's done, the whole code takes around 1.5-2hrs to fully run using the T4 GPU on Google Colab Pro.
# Setting up to run the model on your Windows Machine
- Open Visual Studio Code (VSC)
- Install the Jupyter extension to VSC https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter
  It should also install Jupyter Cell Tags https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vscode-jupyter-cell-tags and Jupyter Keymap extensions https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter-keymap
- Install Python 3.4 as a min, newer the version the better https://www.python.org/downloads/
	- Microsoft may also require you to install python 3 from the Microsoft store (I had to even after changing the PATH environment variables) https://medium.com/@viknesh2798/how-to-fix-the-issues-while-using-python-command-in-the-command-prompt-ba56d9018c5f
	- If pip is not installed follow the instructions in this link to install pip https://www.geeksforgeeks.org/how-to-install-pip-on-windows/
- open command prompt and run ``pip install qtpy tensorflow opencv-python matplotlib pillow seaborn scikit-learn keras-tuner ipykernel``
- Once that's done, go back to VSC and change 2 lines of code to match the below (in 3. Extract Data files to local machine and unzip)
```python
  # Path to the folder containing the zip files in Google Drive
  # zip_files_path = '/content/drive/MyDrive/data/'
  # Path to the folder containing the zip file on local machine
  zip_files_path = 'data'
```

- Finally runn all cells in order excpet 2. Mount Data from Google Drive
	- Alternatively comment out all of 2 and press the "Run All" button at the top.
