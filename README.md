# Image Processing Application using PyQt5
This is a Python application for image processing built with PyQt5. The application provides various image transformation, enhancement, restoration, edge detection, smoothing, and filtering functionalities. Users can load an image, apply different image processing techniques, and visualize the results.

## 1. Features

### **1.1  File Operations**
- **Open:** Load an image from the file system.
- **Save:** Save the processed image to a file.
- **Print:** Print the processed image.
- **Quit:** Exit the application.

### **1.2 Transformation**
- **Rotation**: Rotate the image by 90 degrees.
- **Shearing**: Apply shearing to the image.
- **Translation**: Translate the image.

### **1.3 Image Enhancement**
- **Gray Scale:** Convert the image to grayscale.
- **Negative:** Create a negative of the image.
- **Histogram Equalization:** Enhance image contrast using histogram equalization.
- **Log Transformation:** Apply a logarithmic transformation.
- **Gamma Correction:** Adjust image gamma value for brightness correction

### **1.4 Simple Edge Detection**
- **Hough Transform**: Detect edges using Hough transform.
- **Canny Edge Detection**: Detect edges using the Canny edge detection algorithm.

### **1.5 Cartoon Effect**
- **Cartoon:** Apply a cartoon effect to the image.

### **1.6 Smoothing Filters**
- **Blur:** Apply a blur filter to the image.
- **Box Filter:** Apply a box filter to the image.
- **Median Filter:** Apply a median filter to the image.
- **Bilateral Filter:** Apply a bilateral filter to the image.
- **Gaussian Filter:** Apply a Gaussian filter to the image.

### **1.7 Filters**
- **Median Threshold Filter:** Apply a median threshold filter.
- **Directional Filtering:** Apply directional filtering using a 3x3 kernel.
- **Directional Filtering 2:** Apply directional filtering using a 5x5 kernel.
- **Directional Filtering 3:** Apply directional filtering using a 7x7 kernel.
- **Butterworth Filter:** Apply a Butterworth filter.

### **1.8 Plotting Histogram**
- **Matplotlib Histogram:** Display the histogram of the image.

### **1.9 Zoom**
- **Zoom In:** Enlarge the displayed image for a closer view.
- **Zoom Out:** Reduce the displayed image for a broader view.

### **1.10 About US**
- **About PyQt5:** PyQt5 is a multiplatform C++ GUI toolkit that provides application developers with the functionality to build applications with state-of-the-art graphical user interfaces. It is used as the framework for the graphical user interface of this application.
    
- **About Author:** This application was created and developed by the following individuals:
	- **ThS. Phan Hồ Viết Trường - Instructors**
	- [**tiendung8a6**  (Alex Ngo)](https://github.com/tiendung8a6)
	- [**Kin9989**](https://github.com/Kin9989)
	-	
## 2. How to Run
### **2.1 Clone the Repository:**

```bash 
git clone https://github.com/tiendung8a6/Pixel-Master_Image_Processing_App.git
cd Pixel-Master_Image_Processing_App
```

### **2.2 Install the required packages:**

```bash 
pip install PyQt5 opencv-python numpy scipy matplotlib
```

### **2.3 Run the Application:**:
```bash 
python main.py
```

## 3. How to Use
### **3.1 Open the Application:**
- Run the application using Python.
   
### **3.2 Load an Image:**
- Click on **File > Open** to load an image from your file system.
   
### **3.4 Apply Operations:**
- Explore various operations available in the menu.
- Adjust operation parameters using sliders and input fields.
- Click on the corresponding menu item to apply the selected operation.

### **3.5 Save or Print the Processed Image:**
- After applying desired operations, click on **File > Save** to save the processed image.
- To print the processed image, click on **File > Print**.

### **3.6 Exit the Application:**
- Click on **File > Exit** to exit the application.


## 4. Instructions for converting PyQt applications into executable programs (EXE) on Windows

### **4.1 Reset folder structure**
Program directory structure:

```bash 
|── assets
|  |── main.ui
|  |── open.png
|  |── print.png
|  |── python-icon.png
|  |── save.png
|── main.py
```

In this project:
- The `assets` directory stores all the images used by the program.
- The `main.py` stores the program source code.

### **4.2 Install PyInstaller**
Open Command Prompt or Terminal and execute the following command to install PyInstaller:

```bash 
pip install pyinstaller
``` 

### **4.3 Create Specification File for Application**
Run the following command to create file `.spec`:

```bash 
pyinstaller --name=main --onefile main.py
```

In there:
- `name=main` name the executable file main.exe.
- `onefile` will create a single executable instead of a series of files.

PyInstaller will create a file `main.spec` in the current directory.

### **4.3 Edit the .spec file (optional)**
Open the .spec file with a text editor (e.g. Notepad) and edit if necessary. Configuration options can be added, including paths to image files (`.png`) and user interface (`.ui`) files.

```bash 
a = Analysis(
	['main.py'],
    pathex=[],
    binaries=[],
    datas=[
        ('assets/main.ui', 'main'),
        ('assets/open.png', 'open'),
        ('assets/print.png', 'print'),
        ('assets/python-icon.png', 'python'),
        ('assets/quit.png', 'quit'),
        ('assets/save.png', 'save'),
    ],
```

### **4.4 Build Application**
Run the following command to build the executable:
```bash 
pyinstaller main.spec
```

Once you run this command successfully, you’ll see that PyInstaller creates new directories and files including `build`, `dist`, and `editor.spec`:

```bash 
|── assets
|	|── main.ui
|	|── open.png
|	|── print.png
|	|── python-icon.png
|	|── save.png 
|── build
|	|── main
|	|─ dist
|	|── main
|── main.spec
|── main.py
```
### **4.5 Run Application**
Run the executable from the `dist` folder:

```bash 
cd dist
.\main.exe
```
## Screenshots
