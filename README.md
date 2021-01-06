# ArtGAN: Artwork Restoration using Generative Adversarial Networks

* To install dependences:

<p> Ideally create a new conda enviroment with python==3.6</p>
<p> Then install a GPU-enabled pytorch==1.6.0, torchvision=0.7.0</p>
<p> Finally from the conda env, run the extra dependencies if they are not already satified</p>
<code> pip install -r pip_requirements.txt</code>  
<p></p>

* To train and validate the model per epoch run:

<code> python train.py --model_dir=experiments/base_model --data_dir=/path/to/Dataset </code>

<p>Default value for model_dir is `experiments/base_model`</p>
<p>Change the `/path/to/Dataset` to the correct path of the ArtNet</p>
<p>Also, to change the hyper-parameters, refer to the params.json file since everything is controlled from there.</p>

* To run inference on the model:

<code> python inference.py --model_dir=experiments/base_model --data_dir=/path/to/Dataset -- restore_from=/path/to/best_weights/checkpoint.pth.tar </code>

<p>Change the `/path/to/Dataset` to the correct path of the ArtNet</p>
<p>Change the `/path/to/best_weights/checkpoint.pth.tar` to the correct path of the pre-trained checkpoint (the default value is `experiments/best_model/best_weights/best_after_epoch_163.pth.tar`)</p>

Note that we have included a subset of our own ArtNet dataset for demo purposes, therefore the final results might differ.