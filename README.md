# Compare-Picture-Similarity
using picture structural similarity index in product matching.

### Required Libraries
analysis was performed using Python 3 at Kaggle Notebook. Please make sure that the followings libraries is already installed in your libraries:
1. os
2. cv2
3. pandas
4. numpy
5. match
6. decimal
7. tensorflow
8. skimage
9. expects

### About Data
The data are the secondary data took from XYZ Company for their ecommerce product.
1. new_training_set.csv: List of product title pairs, respective images and their labels (“match” or ”different_product”).
• File of 6 columns and 10181 rows, for each row:
- Column 1 - pair_index: title pair row index
- Column 2 - title_1: title of the first product
- Column 3 - image_1: image file name of the image for the first product
- Column 4 - title_2: title of the second product
- Column 5 - image_2: image file name of the image for the second product
- Column 6 - pair label: 1 or 0 (1 means “match” and 0 means “different product”)
2. Training_img.zip: containing images for each of the products.

### Description
structural similarity index (SSIM) was first introduced in the 2004 IEEE paper, Image Quality Assessment: From Error Visibility to Structural Similarity. The abstract provides a good intuition into the idea behind the system proposed,
"Objective methods for assessing perceptual image quality traditionally attempted to quantify the visibility of errors (differences) between a distorted image and a reference image using a variety of known properties of the human visual system. Under the assumption that human visual perception is highly adapted for extracting structural information from a scene, we introduce an alternative complementary framework for quality assessment based on the degradation of structural information". For the detail about SSIM click this following Link [SSIM](https://medium.com/srm-mic/all-about-structural-similarity-index-ssim-theory-code-in-pytorch-6551b455541e).

### Result
From the research conducted it was concluded that the SSIM index was easily to compare two picture. To predict is two picture is similiar or not from the SSIM, Logistic regression modeling is one of the best method to find out SSIM threshold compare to decision tree, Gaussian NB and SVC method with Accuracy 0.75 and F1 score 0.75.
