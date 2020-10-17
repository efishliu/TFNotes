* **下载数据文件并解压缩**  
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

* **加载数据**  
```python  
    import pandas as pd
    data = pd.read_csv(csv_path)  #返回一个dataframe
```

* **DateFrame常用操作**  
```python
    data.head() #查看前5行
    data.info() #查看data结构（行数，列名，列存储类型）
    data.describe() #查看一些数值特征（count,mean,min,max,std)
    
```

* **随机切分训练集与测试集**  
```python
    from sklearn.model_selection import train_test_split
    
    train_set,test_set = train_test_split(data,test_size=0.2,random_state=42)
```


