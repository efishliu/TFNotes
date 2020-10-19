* **创建运行环境与安装**  
```shell  
    conda env list #查看虚拟环境
    conda create -n [env_name] python=3.6 #创建python虚拟环境
    source activate [env_name] #激活虚拟环境
    source deactivate [env_name] #关闭虚拟环境
    conda remove -n [env_name] --all #删除虚拟环境
    #安装基础环境
    conda install numpy pandas scipy scikit-learn matplotlib
    #安装tensorflow
    conda install tensorflow
    
