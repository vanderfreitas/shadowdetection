# Automatic shadow detection in aerial and terrestrial images


**Abstract**: Shadows exist in almost all aerial and outdoor images, and they can be useful for estimating Sun position estimation or measuring object size. On the other hand, they represent a problem in processes such as object detection/recognition, image matching, etc., because they may be confused with dark objects and change the image radiometric properties. We address this problem on aerial and outdoor color images in this work. We use a filter to find low intensities as a first step. For outdoor color images, we analyze spectrum ratio properties to refine the detection, and the results are assessed with a dataset containing ground truth. For the aerial case we validate the detections depending of the hue component of pixels. This stage takes into account that, in deep shadows, most pixels have blue or violet wavelengths because of an atmospheric scattering effect.

**Authors**: Vander L. S. Freitas, Barbara M. F. Reis and Antonio M. G. Tommaselli.


Please cite this publication, if you use the code:

+ FREITAS, V. L. S.; REIS, B. M. F.; TOMMASELLI, A. M. G. Automatic shadow detection in aerial and terrestrial images. Boletim de Ciências Geodésicas, v. 23, n. 4, 2017. ISSN 1413-4853.

  + [Click here to download the Paper](https://revistas.ufpr.br/bcg/article/view/56798/34173)


Dependency: [OpenCV](https://docs.opencv.org/master/d2/de6/tutorial_py_setup_in_ubuntu.html)


Example:

```python
import cv2
import shdwDetection as sd

imgRef = cv2.imread("DSC01641.jpg")
imgOut = sd.shadowDetection_Santos_KH(imgRef)
cv2.imwrite("DSC01641_shdw.pgm", imgOut)
```
