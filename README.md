# chainer-test

It is test scripts of chainer and dockerfiles for its test environment.


## Requiements

- nvidia-docker
- Docker (>=1.6)
- CUDA 7.5

## How to use

Run test scripts with options that specify the environment to test.

```
$ ./run_install_test.py --base=ubuntu14_py2 --numpy=numpy19 --cuda=cuda70 --cudnn=cudnn2
```

These test scripts create `Dockerfile`, make containers, and run appropriate test scripts.


## Scripts to run

- `run_install_test.py`: Installation test.
- `run_test.py`: Build and run test scripts.
- `run_multi_test.py`: Build and run test scripts with .


## In Jenkins

Make a multi-configuration project.
In the matrix configuration, make four variables, `BASE`, `CUDA`, `CUDNN` and `NUMPY`.
You can make a configuration matrix for all combination.
