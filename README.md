# Dimensionality Reduction in Images  

This project aims to implement **dimensionality reduction methods in images**, converting color images to **grayscale** and performing **binarization** (black and white).  
The approach used **does not rely on pre-built libraries** for this processing, ensuring an implementation from scratch.  

---

## Project Objectives  

- Create a **manual function** for converting color images to **grayscale**.  
- Create a **manual function** to binarize the image (convert to **black and white**).  
- Allow **automatic processing** of multiple images.  
- **Save the results** in the `/content/data/output/` folder for easy access.  
- **Do not use libraries** that already perform these processes directly (OpenCV, PIL, etc.).  

---

## Project Structure  

📁 `data/input/` - Folder containing color images for testing.  
📁 `data/output/` - Processed results (grayscale and binarized images).  
📁 `notebooks/` - Jupyter Notebook with processing code.   
📄 `README.md` - This file.  

---

## Implementation  

### **Grayscale Conversion**  
The conversion is based on the **luminance formula**:  
  
  0.299 * R + 0.587 * G + 0.114 * B  
  
This generates a monochromatic image representing the brightness intensity of each pixel.  

### **Image Binarization**  
Binarization applies a **fixed threshold (128)**:  
- Pixels above 128 → **White (255)**  
- Pixels below 128 → **Black (0)**  

This process enhances contours and important shapes in the image.  

---

## How to Run the Code on Google Colab  

1. **Create a notebook in Colab**.  
2. **Upload images to `/content/data/input/`**.  
3. **Run the code to automatically convert all images**.  
4. **Converted files will be saved in the `/content/data/output/` folder**.  

For more details, check the Jupyter Notebook code.  

---

## Challenges Faced and Solutions  

### **Loss of Information in Grayscale Conversion**  
 The equation was adjusted to correctly weight the RGB channels and retain important details.  

### **Threshold Adjustment in Binarization**  
 The value **128** was chosen as the default but can be dynamically adjusted based on the image histogram.  

---

## Technologies Used  

- **Python** - The main programming language of the project.  
- **Matplotlib** - For visualizing images before and after processing.  
- **NumPy** - For array manipulation and numerical calculations.  
- **Jupyter Notebook / Google Colab** - For interactive development.  

---

## Contributions  

 Want to contribute to the project? Follow the steps below:  

1. Fork the repository.  
2. Create a **new branch**:  
   ```bash
   git checkout -b feature-my-feature
   ```
3. Make your changes and commit:
    ```
    git commit -m 'Add new functionality'
    ```
4. Push your changes:
    ```
    git push origin feature-my-feature
    ```
5. Open a Pull Request.

## 📜 License

This project is licensed under the MIT License.
