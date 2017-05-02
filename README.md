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

#### Run tensorboard

- `tensorboard --logdir=path/to/logs`

- In Jupyter notes

  ```python
  import tensorflow as tf
  summary = tf.summary.scalar("foo", 42.0)

  with tf.Session() as session:
      writer = tf.summary.FileWriter("path/to/logs", session.graph)
      summaries = session.run(summary)
      writer.add_summary(summaries, 1)
      writer.close()
  ```
- Navigate to `https://localhost:6006 to see the graph
