#NaroNet-method-testing

##how it goes: 
- get access to cluster
- get familiar with cluster
- create git repository 
- read the [NaroNet paper] (https://www.sciencedirect.com/science/article/pii/S1361841522000366) 
- check out the NaroNet [git] (https://github.com/djimenezsanchez/NaroNet/blob/main/README.md)
- create conda env(NaroNet3) on the cluster using YAML file (+install mmissing depencensies manually)


<div class="highlight">
    <pre tabindex="0" class="chroma">
        <code class="language-fallback" data-lang="fallback">
            conda env create -f NaroNet3.yml 
            conda install pytorch torchvision -c pytorch
            conda install -c conda-forge sklearn-pandas
        </code>
    </pre>
</div>



you could run pip install NaroNet with my conda env activated. this allows to build naronet. but the package version does not correspond to the git version, so instead i will be cloning the git repository to my cluster and working with it there. 


running: 
<div class="highlight">
    <pre tabindex="0" class="chroma">
        <code class="language-fallback" data-lang="fallback">
           from NaroNet.utils.DatasetParameters import parameters
from NaroNet.Patch_Contrastive_Learning.patch_contrastive_learning import patch_contrastive_learning
from NaroNet.Patch_Contrastive_Learning.preprocess_images import preprocess_images
from NaroNet.architecture_search.architecture_search import architecture_search
from NaroNet.NaroNet import run_NaroNet
from NaroNet.NaroNet_dataset import get_BioInsights
        </code>
    </pre>
</div>

need to install more dependencies: 
(NaroNet3) [hd_vb248@o05i15 architecture_search]$ pip install -U "ray[data,train,tune,serve]"
(NaroNet3) [hd_vb248@o05i15 architecture_search]$ pip install torch-geometric
(NaroNet3) [hd_vb248@o05i15 architecture_search]$ conda install pytorch-scatter -c pyg

for newer versions of ray[tune] "ray.tune.suggest" will not work, so the architecture_search file had to be edited to "ray.tune.search" 


