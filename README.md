#### Install using anaconda

- Follow the steps from [here](https://docs.continuum.io/anaconda/install-macos.html#macos-graphical-install)
- Add PATH `export PATH="/Users/username/anaconda/bin:$PATH"`
- `conda create -n tensorflow2 python=2.7`
- `source activate tensorflow2`
- `conda install -c conda-forge tensorflow`
- `conda install notebook ipykernel`
- `jupyter notebook`
- Open new notebook, Choose Python 2 and try the below,
  ```python
  import tensorflow as tf
  hello = tf.constant('Hello, TensorFlow!')
  sess = tf.Session()
  print(sess.run(hello))
  ```