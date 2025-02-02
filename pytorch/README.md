Install PyTorch from source with pip and cudnn.


```
pip install -U --user numpy pyyaml typing keras scipy future matplotlib typing_extensions ipython opencv-python pygame
```

2) Install cudnn

```
tar -xzvf cudnn-9.0-linux-x64-v7.tgz
sudo cp cuda/include/cudnn.h /usr/local/cuda/include
sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64
sudo chmod a+r /usr/local/cuda/include/cudnn.h /usr/local/cuda/lib64/libcudnn*
```

3) Install PyTorch

```
git clone --recursive https://github.com/pytorch/pytorch
cd pytorch
python setup.py install --user
```

4) Install Vision

```
git clone https://github.com/pytorch/vision
cd vision
sudo python setup.py install --user
```

Run

```
cd examples/super_resolution/
python main.py --upscale_factor 3 --batchSize 4 --testBatchSize 100 --nEpochs 1 --lr 0.001

cd examples/word_language_model/
python main.py --cuda --emsize 650 --nhid 650 --dropout 0.5 --epochs 40   
```


git clone https://github.com/pytorch/examples
