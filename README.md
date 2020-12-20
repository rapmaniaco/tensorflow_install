<h4>Referências</h4>

<ul>
<li>https://medium.com/@karol_majek/10-simple-steps-to-tensorflow-object-detection-api-aa2e9b96dc94</li>
<li>https://medium.com/@teyou21/setup-tensorflow-for-object-detection-on-ubuntu-16-04-e2485b52e32a</li>
<li>https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2.md</li>
</ul>

```
git clone https://github.com/tensorflow/tensorflow
cd tensorflow
git clone https://github.com/tensorflow/models
```
```
sudo apt-get install protobuf-compiler python-pil python-lxml python-tk
pip3 install Cython
pip3 install contextlib2
pip3 install jupyter
pip3 install matplotlib
pip3 install  pandas
```

<h4>Install COCO API</h4>
<p>We will need to for model evaluation, but it is a good idea to install it just now. Change <path_to_tensorflow> to path to your Tensorflow repository.</p>

```
git clone https://github.com/cocodataset/cocoapi.git
cd cocoapi/PythonAPI
make
cp -r pycocotools /home/edee/EdeE/Processamento_Imagem/TF_github/tensorflow/models/research/
```

<h4>Install protoc</h4>

```
cd /home/edee/EdeE/Processamento_Imagem/TF_github/tensorflow/models/research
protoc object_detection/protos/*.proto --python_out=.

```

<h4>Install object detection</h4>

```
nano ~/.bashrc
#TensorFlow - Adicionar na ultima linha
export PYTHONPATH=$PYTHONPATH:/home/edee/EdeE/Processamento_Imagem/TF_github/tensorflow/models/research/:/home/edee/EdeE/Processamento_Imagem/TF_github/tensorflow/models/research/slim
source ~/.bashrc
```

<h4>Jupyter</h4>

```
pip install notebook
```

<h4>Testando exemplo</h4>


