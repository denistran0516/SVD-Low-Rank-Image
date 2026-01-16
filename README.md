This and the next challenge involve taking the SVD of a picture. A picture is represented
as a matrix, with the matrix values corresponding to grayscale intensities of the pixels. We will use a
picture of Einstein. You can download the file here1. Of course, you can replace this with any other
picture—a selfie of you, your dog, your kids, your grandmother on her wedding day2... However, you
may need to apply some image processing to reduce the image matrix from 3D to 2D (thus, grayscale
instead of RGB) and the datatype must be floats (Python).
(a) After importing the image, constructed a low-rank approximation (based on the SVD layer
decomposition, see lecture note) using various numbers of singular values. Show the original and
low-rank approximations side-by-side. Tested various numbers of components and qualitatively evaluate
the results.
(b) Created a scree plot of the percent-normalized singular values. Then test various thresholds for
reconstructing the picture (e.g., including all components that explain at least 4% of the variance).
What threshold seems reasonable? The main additions here are computing percent variance explained
and thresholding. It’s a good idea to check that all of the normalized singular values sum to 100.
>> # convert singular value s to percent explained: s = 100* s /np .sum( s )
