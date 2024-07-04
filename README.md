# Receipt Rocket


Effortlessly extract detailed information from multi-item receipts using advanced computer vision and image processing. No machine learning or deep learning needed—just pure image processing magic!

## Features

- **Efficient Segmentation**: Isolates and identifies receipts from multi object images
- **Perspective Restoration**: Automatically corrects the perspective of scanned receipts.
- **Text Extraction** : Leveraging Tesseract to extract text using regular expressions.
- **Pure Image Processing**: Leveraging the power of computer vision without the complexity of ML/DL models.

## Important Functions
* `approximate_counter(counter)` : This function takes a contour as input and approximates it to a polygon with fewer vertices based on the specified precision. The cv2.approxPolyDP function approximates the contour to another shape with fewer vertices. The second argument, 0.032 * peri, is the approximation accuracy parameter, which specifies the maximum distance between the original contour and its approximation.

## Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/rakesh018/Receipt-Rocket.git
cd Receipt-Rocket
