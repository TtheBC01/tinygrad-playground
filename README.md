# Tinygrad Playground
Playing around w/ tinygrad framework. This repo uses the docker environment from [CudaConda3](https://github.com/TtheBC01/CudaConda3) for NVidia GPU support. 

## Fire up the environment 

To start up the containerized environment, run the following commands to build the tinygrad environment and then start a container w/ a Jupyter notebook environment. 

```
docker build -t tinygrad .
docker run --name tinygrad --rm -p 8888:8888 -d --gpus all tinygrad
```

If you want to mount your local directory to save your work to disk between docker session, use the volume flag:

```
docker run -v .:/root --name tinygrad --rm -p 8888:8888 -d --gpus all tinygrad
```

Then go to http://localhost:8888/jupyter/lab to see you notebook session. 