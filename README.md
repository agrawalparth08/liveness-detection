# liveness-detection
A repository to compare and contrast different methods for liveness detection and trying an ensemble method in the end to avoid L1 and L2 spoofing stated as benchmark on liveness.com

# Literature and Inspiration

## Adrian Rosenbrock's [article][1] on Liveness detection - 

The approaches he mentioned are the ones which are used today mostly for this problem statement.

1. __Texture analysis__ - Computing Local Binary Patterns (LBPs) over face regions and using an SVM to classify the faces as real or spoofed.

2. __Frequency analysis__ - Examining the Fourier domain of the face.

3. __Variable focusing analysis__- Examining the variation of pixel values between two consecutive frames.

4. __Heuristic-based algorithms__ - Eye movement, lip movement, and blink detection. These set of algorithms attempt to track eye movement and blinks to ensure the user is not holding up a photo of another person (since a photo will not blink or move its lips).

5. __Optical Flow algorithms__ - Examining the differences and properties of optical flow generated from 3D objects and 2D planes.
3D face shape, similar to what is used on Apple’s iPhone face recognition system, enabling the face recognition system to distinguish between real faces and printouts/photos/images of another person.

6. __Combinations of the above__ - Enabling a face recognition system engineer to pick and choose the liveness detections models appropriate for their particular application.

## iBeta Liveness quality ISO [Standards][2]
[1]: https://www.pyimagesearch.com/2019/03/11/liveness-detection-with-opencv/
[2]: https://liveness.com/
