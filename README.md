# iNaturalist_Robustness

Extracting images with spurious correlation in Image Classification is very important for measuring model robustness. I define robustness with the following equation;

Suppose that 
sp       : spurious correlation image.
nsp      : non sp image. 
Xsp      : total number of sp in the whole population. 
MXsp     : mis-classified sp. 

robustness = Msp / Xsp. (accuracy in the population of sp images)


Most important publication on image classification robustness measure it on either synthetic or some benchmark dataset in a different domain [1] . I think that this method lacks objectivity and relevance because its robustness not domain adaption being addrressed. I am focused on animal classification problems like iNaturalist data. It is very important to know wether your model is learning on spurious correlations of animal backgrounds and environemnt or the shapes and features of the animals (relevant features). 

Hence I have developed code "ImageClustering_V4_1.ipynb" to extract images where model predictions was mainly based on spurious correlation (sp) like images in folder "noisy_images". The code addresses only a very small sample of 500 images from iNaturalist where the actual dataset can go up to 500K images around 200 GB of training data. The code base can be re-adjusted though to scale up to whatever number of images. All in all it is a one of a kind so far in this field. You may read more about the approaach here [2].

I hope you can find utility in this codebase and if you have any questions or need any explanation , please reach me at emad.ezzeldin4@gmail.com.


[1] https://arxiv.org/pdf/1907.02893.pdf
[2] https://medium.com/p/2fb7c518930b
