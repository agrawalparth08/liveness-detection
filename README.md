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

# Algorithms

1. __High res face masks with eyes and lips and nose cutouts__ 
    
    Color Texture Analysis [Paper][3] [Matlab Code][4]
    
2. __Deep Learning CNN Approach__ - 

    1. LivenessNet [Pyimagesearch][1] 
    
    2. Model 3 proposed in this [paper][5] and [source code][6] on CASIA-FASD Dataset.
        The dataset has some restrictions of access. Try VPN (Southeast Asia) and registering [here][7]
        
3. __Red Eye + Texture Analysis__

    This is a proposed approach which takes into consideration the hardware on which the face detection is to be run.
    
    Some references -
    
    1. [Selfie Flash][8] which gave me the idea that you don't need front flash in mobile device
        
    2. [Red Eye Effect][9] which takes away blinking plus video specific spoofing
        
    3. [Face Texture][10] found from the very interesting comparison [paper][11] for liveness detection 
     
    
![alt text][algo]

[algo]:  https://github.com/agrawalparth08/liveness-detection/blob/master/algorithm.jpg "Fusion Algorithm"

[1]: https://www.pyimagesearch.com/2019/03/11/liveness-detection-with-opencv/
[2]: https://liveness.com/
[3]: https://www.researchgate.net/publication/301571761_Face_Spoofing_Detection_Using_Colour_Texture_Analysis
[4]: https://github.com/zboulkenafet/Face-anti-spoofing-based-on-color-texture-analysis
[5]: https://ieeexplore.ieee.org/document/8166863
[6]: https://github.com/houliang428/CNN-for-face-anti-spoofing
[7]: http://biometrics.idealtest.org/findTotalDbByMode.do?mode=Face
[8]: https://play.google.com/store/apps/details?id=com.reactivstudios.android.selfieflash&hl=en_IN
[9]: https://www.goodeyes.com/blog/red-eyes-photos/
[10]: https://yonsei.pure.elsevier.com/en/publications/face-liveness-detection-based-on-texture-and-frequency-analyses
[11]: https://arxiv.org/pdf/1405.2227
