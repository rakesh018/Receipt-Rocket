# Receipt Rocket


Effortlessly extract detailed information from multi-item receipts using advanced computer vision and image processing. No machine learning or deep learning needed—just pure image processing magic!

## Features

- **Efficient Segmentation**: Isolates and identifies receipts from multi object images
- **Perspective Restoration**: Automatically corrects the perspective of scanned receipts.
- **Text Extraction** : Leveraging Tesseract to extract text using regular expressions.
- **Pure Image Processing**: Leveraging the power of computer vision without the complexity of ML/DL models.

## Important Functions
* `approximate_contour(contour)` : This function takes a contour as input and approximates it to a polygon with fewer vertices based on the specified precision. The cv2.approxPolyDP function approximates the contour to another shape with fewer vertices. The second argument, 0.032 * peri, is the approximation accuracy parameter, which specifies the maximum distance between the original contour and its approximation.

* `get_receipt_contour(contours)` : Responsible for identifying receipt. Out of all top 10 contours with largest area, it selects the contour which has 4 vertices after approximation (Rectangle).

* `contour_to_rect(contour)` : This function finds the clockwise ordering (top-left,top-right,bottom-right,bottom-left) of the vertices using simple mathematical reasoning (sum and difference of coordinates).

* `wrap_perspective(image,rect)` : This function calculates Transformation Matrix and maps the points on image from input plane to new output plane.

* `find_amounts(text)` : This function utilizes regular expression to search for targetted text in the tesseract output.

## Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/rakesh018/Receipt-Rocket.git
cd Receipt-Rocket

## Future Work

There are several potential avenues for future development and improvement:

- **Enhanced Model Performance:** Continuously optimize the models for better accuracy and efficiency.
- **Integration of Deep Learning:** Explore the integration of deep learning techniques to further improve recognition accuracy.
- **Real-Time Processing:** Implement real-time processing capabilities for quicker response times.
- **User Interface Enhancement:** Develop a user-friendly interface for easier interaction and visualization of results.
- **Data Augmentation and Expansion:** Increase the dataset size and diversity through data augmentation techniques.
- **Deployment and Scalability:** Prepare the model for deployment in scalable environments, considering cloud solutions for flexibility.

These areas represent opportunities to advance the current implementation and enhance its practical utility.
