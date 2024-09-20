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


conda install cuda-cudart cuda-version=12



you could run pip install NaroNet with my conda env activated. this allows to build naronet. but the package version does not correspond to the git version, so instead i will be cloning the git repository to my cluster and working with it there. 


