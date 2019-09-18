# FusionNet

Demonstration source code using the webcam for palmprint and finger texture recognition.
The algorithms used in the code are based on the paper:

	A. Genovese, V. Piuri, F. Scotti, and S. Vishwakarma, 
    "Touchless palmprint and finger texture recognition: A Deep Learning fusion approach", 
    2019 IEEE Int. Conf. on Computational Intelligence & Virtual Environments for Measurement Systems and Applications (CIVEMSA 2019),
    Tianjin, China, June 14-16, 2019
	
Project page:

	http://iebil.di.unimi.it/fusionnet/index.htm

Outline:
![Outline](http://iebil.di.unimi.it/fusionnet/imgs/outline.png "Outline")

Citation:

    @InProceedings {civemsa19,
        author = {A. Genovese and V. Piuri and F. Scotti and S. Vishwakarma},
        booktitle = {Proc. of the 2019 IEEE Int. Conf. on Computational Intelligence & Virtual Environments for Measurement Systems and Applications (CIVEMSA 2019)},
        title = {Touchless palmprint and finger texture recognition: A Deep Learning fusion approach},
        address = {Tianjin, China},
        month = {June},
        day = {14-16},
        year = {2019},
    }

Main files:

    - launch_Demo_FusionNet.m: main file

Main directories:

    - ./dirDB: directory where template are stored
    - ./models: directory where pretrained models are saved

Requirements:

    - A webcam
    The code is preconfigured to use an integrated webcam. 
    Change lines 51-52 of "launch_Demo_FusionNet.m" to change webcam
    %cam = webcam('integrated');
    %cam.Resolution = '640x480';

Procedure:

    1) launch main file and choose 'e' for enrolling individuals
        a) choose a name for the individual
        b) capture the background without body parts and moving objects
        c) capture the left hand sideways, placing the hand inside the red box (see "./demo_images/hand_acquisition.png")
        d) repeat acquisition until 3 successful acquisitions are performed
    2) launch main file to enroll as many individuals as needed
    3) launch main file and choose 'r' for recognition
    
Part of the code uses the Matlab source code of the paper:

	T. Chan, K. Jia, S. Gao, J. Lu, Z. Zeng and Y. Ma, 
	"PCANet: A Simple Deep Learning Baseline for Image Classification?," 
	in IEEE Transactions on Image Processing, vol. 24, no. 12, pp. 5017-5032, Dec. 2015.
	DOI: 10.1109/TIP.2015.2475625
    http://mx.nthu.edu.tw/~tsunghan/Source%20codes.html
	
and the export_fig library:

	Yair Altman, 
	"export_fig", 2018, 
	https://it.mathworks.com/matlabcentral/fileexchange/23629-export_fig



	