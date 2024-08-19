# ORC-TASK01

Link to install tesseract = https://github.com/UB-Mannheim/zotero-ocr (Go to the readme file and you'll find the link)

Steps Involved:

1) Loading the Image:
The image is loaded from a specified path using OpenCV's cv2.imread() function.

2) Converting to Grayscale:
The image is converted to a grayscale image using cv2.cvtColor(). Grayscale conversion simplifies the image data, making it easier to process for text extraction.

3) Image Preprocessing:
For printed text, a binary thresholding method is applied to the grayscale image using cv2.threshold(). This step converts the image into a binary format where text is highlighted.
For handwritten text, an adaptive thresholding technique (commented out in the code) can be used instead. This method adjusts the threshold dynamically across the image, which is particularly useful for non-uniform lighting conditions.

4) Text Extraction:
The processed image is passed to Tesseract, which is used to extract the text. The pytesseract.image_to_string() function performs the OCR, returning the detected text in the image.

5) Display the Processed Image:
The processed binary image is displayed using Matplotlib, allowing you to visually inspect the result of the preprocessing.
