* 下载数据文件并解压缩  
```python  
    import os
    import urllib
    import tarfile
    
    download_url = "http://raw.githubusercontent.com/.."
    #创建存放目录
    datasets_path = os.path.join("datasets")
    os.makedirs(datasets_path,exist_ok=True)
    data_path = os.path.join(datasets_path,"data.tgz")
    #下载压缩文件
    urllib.request.urlretrieve(download_url,datapath)
    #解压缩文件
    data_tgz = tarfile.open(data_path)
    data_tgz.extractall(path=datasets_path)#解压缩路径
    data_tgz.close()
```
