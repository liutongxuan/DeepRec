# DeepRec Java 源代码编译

## 开发环境准备

**CPU Base Docker Image**

```
registry.cn-shanghai.aliyuncs.com/pai-dlc-share/deeprec-developer:deeprec-base-cpu-py36-ubuntu18.04
```

Docker Hub repository
```
alideeprec/deeprec-base:deeprec-base-cpu-py36-ubuntu18.04
```

**GPU(cuda11.0) Base Docker Image**

```
registry.cn-shanghai.aliyuncs.com/pai-dlc-share/deeprec-developer:deeprec-base-gpu-py36-cu110-ubuntu18.04
```

Docker Hub repository
```
alideeprec/deeprec-base:deeprec-base-gpu-py36-cu110-ubuntu18.04
```

## 代码编译

**配置环境变量-编译GPU**
```
export TF_CUDA_COMPUTE_CAPABILITIES="7.5,8.0"
```

```bash
./configure
```

**GPU/CPU版本编译**

```bash
bazel build --config opt //tensorflow/java:tensorflow //tensorflow/java:libtensorflow_jni
```
