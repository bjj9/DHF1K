# DHF1K


===========================================================================

W. Wang, J. Shen, F. Guo, M.-M Cheng and A. Borji, 

Revisiting Video Saliency: A Large-scale Benchmark and a New Model,  

IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2018  

===========================================================================

The code (ACLNet) and dataset (DHF1K with raw gaze records, UCF-sports are new added!) can be downloaded from:

Google disk：https://drive.google.com/open?id=1sW0tf9RQMO4RR7SyKhU8Kmbm4jwkFGpQ

Baidu pan: https://pan.baidu.com/s/110NIlwRIiEOTyqRwYdDnVg

The Hollywood-2 (74.6G, including attention maps) can be downloaded from:

Google disk：https://drive.google.com/file/d/1vfRKJloNSIczYEOVjB4zMK8r0k4VJuWk/view?usp=sharing


===========================================================================

Files:

'video': 1000 videos (videoname.AVI)

'annotation/videoname/maps': continuous saliency maps in '.png' format

'annotation/videoname/fixation': binary eye fixation maps in '.png' format

'annotation/videoname/maps': binary eye fixation maps stored in mat file

'generate_frame.m': used for extracting the frame images from AVI videos. 

Note that please do not change the way of naming frames.

===========================================================================

Dataset splitting:

Training set:   first 600 videos (001.AVI-600.AVI)

Validation set: 100 videos (601.AVI-700.AVI)

Testing set:    300 videos (701.AVI-1000.AVI)


The annotations for the training and val sets are released, but the 

annotations of the testing set are held-out for benchmarking.

===========================================================================

We have corrected some statistics of our results 
(baseline training setting (iii)) on UCF sports dataset.
Please see our newest version in ArXiv.

===========================================================================

Note that, for Holly-wood2 dataset, we used the split videos 
(each video only contains one shot), instead of the full videos.

===========================================================================

The raw data of gaze record has been uploaded.

===========================================================================

For DHF1K dataset, we use following functions to generate continous saliency map:

[x,y]=find(fixations);

densityMap= make_gauss_masks(y,x,[video_res_y,video_res_x]); 

make_gauss_masks.m has been uploaded.

For UCF and Hollywood, I directly use following functions:

densityMap = imfilter(fixations,fspecial('gaussian',150,20),'replicate');

===========================================================================

Results submission.

Please orgnize your results in following format:

yourmethod/videoname/framename.png

Note that the frames and framenames should be generated by 'generate_frame.m'.

Then send your results to 'DHF1Kdataset@gmail.com'. 

You can only sumbmit ONCE within One week. 

Please first test your model on the val set or other video saliency dataset.

The response may be more than one week.

If you want to list your results on our web, please send your name, model 

name, paper title, short description of your method and the link of the web

of your project (if you have).

===========================================================================

Citation:

	@inproceedings{wang2018revisiting,
  		title={Revisiting Video Saliency: A Large-scale Benchmark and a New Model},
  		author={Wang, Wenguan and Shen, Jianbing and Guo, Fang and Cheng, Ming-Ming and Borji, Ali},
  		booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
  		year={2018},
	}

If you find our dataset is useful, please cite above paper.

===========================================================================

Code (ACLNet): 

You can find the code in google disk:  https://drive.google.com/open?id=1sW0tf9RQMO4RR7SyKhU8Kmbm4jwkFGpQ

===========================================================================

Contact Information
Email:

	wenguanwang.ai@gmail.com
	
	shenjianbing@bit.edu.cn
------------------------------------------------------------------------------------------------
