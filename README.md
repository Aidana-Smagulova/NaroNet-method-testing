#NaroNet-method-testing
get access to cluster 

then create conda env 

create a naronet env 
same a git but with 
pip install opencv-python and pip install opencv-contrib-pytho instead of sudo apt 

ask for a job with salloc 
go to the naronet environmnet 
pip install kernel 
create a kernel
create a jyputer lab server 
connect to the server with visual studio code and to your kernel 


<div class="highlight">
    <pre tabindex="0" class="chroma">
        <code class="language-fallback" data-lang="fallback">
            conda env create -f Narp.yml 
            conda install pytorch torchvision -c pytorch
        </code>
    </pre>
</div>


conda install pandas>=1.1.5 tifffile>=2020.2.16 

conda install scikit-learn scikit-image

conda install Pillow

conda install matplotlib>=3.2.1 

conda install numpy>=1.18.2

conda install scipy>=1.5.4

conda install -c conda-forge pycox
 
conda install -c conda-forge sklearn-pandas

conda install -c anaconda torchtuples

pip install opencv-contrib-python

pip install opencv-python

 conda install tqdm
 
pip install ray[tune]

conda install xlsxwriter

(conda install -c conda-forge argparse - not needed if you have python version 3* and higher, it's pre-installed )

conda install -c conda-forge imbalanced-learn
 
conda install pytorch torchvision -c pytorch

conda install xlsxwriter imgaug xlrd

conda install hyperopt imagecodecs

conda install -c conda-forge tensorboard

conda install -c conda-forge tensorflow
 
conda install cuda-cudart cuda-version=12




after this i added the NaroNet-0.0.11 tar zip file into my naronet workspace on cluster 

and ran pip install NaroNet with my conda env activated. this let me install missing packages and build naronet. 




create a cona environment for NaroNet using yml file: 
yml: 
name: NaroNet3
channels: 
- anaconda  
- conda-forge
- defaults 
- pytorch 
dependencies: 
- python=3.8
- 'matplotlib>=3.2.1'
- 'pandas>=1.1.5'
- 'seaborn>=0.11.0'
- 'scikit-learn'
- 'scikit-image'
- 'Pillow'
- 'scipy>=1.5.4'
- 'numpy>=1.18.2'
- 'tifffile>=2020.2.16'
- 'pycox>=0.2.0'
- 'torchtuples>=0.2.0'
- 'tqdm>=4.50.2'
- 'imbalanced-learn'
- 'xlsxwriter>=1.1.5'
- 'imgaug>=0.4.0'
- 'xlrd>=1.2.0'
- 'hyperopt>=0.2.3'
- 'imagecodecs'
- 'tensorboard>=1.14.0'
- 'tensorflow>=1.14.0'
- 'pip'
- 'jupyterlab'
- 'ipykernel'
- 'notebook'
- pip:
  - 'ray[tune]' 
  - 'opencv-python>=4.2.0'





