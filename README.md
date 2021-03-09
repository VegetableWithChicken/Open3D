<p align="center">
<img src="https://raw.githubusercontent.com/intel-isl/Open3D/master/docs/_static/open3d_logo_horizontal.png" width="320" />
</p>

# 说明    
考虑到中国境内通过git clone 或则 VPN方式下载thirdparty库很困难，我fork官方库之后对文件做了修改，这样可以方便在国内进行下载.    
Windows 或则linux系统可以使用以下方式clone文件:  

* 1，git clone --recursive https://github.com.cnpmjs.org/VegetableWithChicken/Open3D.git  
* 2，由于Eigen模块缺失，可以去官网下载release之后放入Open3D\3rdparty\Eigen文件夹即可  
* 3，缺少pybind11文件：删除 Open3D\3rdparty\pybind11文件夹，然后右击open3d文件夹，git clone https://github.com.cnpmjs.org/pybind/pybind11.git 即可下载  
* 4，其他文件夹有问题，可以使用相同方式clone , 需要把https://github.com/改为 https://github.com.cnpmjs.org/之后再进行git clone操作  
* 5，如果VS编译文件，出现找不到文件情况，应该是库链接错误，按照VS链接库方式正确link库即可  

# Open3D: A Modern Library for 3D Data Processing

<h4>
    <a href="http://www.open3d.org">Homepage</a> |
    <a href="http://www.open3d.org/docs">Docs</a> |
    <a href="http://www.open3d.org/docs/release/getting_started.html">Quick Start</a> |
    <a href="http://www.open3d.org/docs/release/compilation.html">Compile</a> |
    <a href="http://www.open3d.org/docs/release/index.html#python-api-index">Python</a> |
    <a href="http://www.open3d.org/docs/release/cpp_api.html">C++</a> |
    <a href="https://github.com/intel-isl/Open3D-ML">Open3D-ML</a> |
    <a href="https://github.com/intel-isl/Open3D/releases">Viewer</a> |
    <a href="http://www.open3d.org/docs/release/contribute/contribute.html">Contribute</a> |
    <a href="https://www.youtube.com/channel/UCRJBlASPfPBtPXJSPffJV-w">Demo</a> |
    <a href="https://forum.open3d.org">Forum</a>
</h4>

Open3D is an open-source library that supports rapid development of software
that deals with 3D data. The Open3D frontend exposes a set of carefully selected
data structures and algorithms in both C++ and Python. The backend is highly
optimized and is set up for parallelization. We welcome contributions from
the open-source community.

[![Ubuntu CI](https://github.com/intel-isl/Open3D/workflows/Ubuntu%20CI/badge.svg)](https://github.com/intel-isl/Open3D/actions?query=workflow%3A%22Ubuntu+CI%22)
[![macOS CI](https://github.com/intel-isl/Open3D/workflows/macOS%20CI/badge.svg)](https://github.com/intel-isl/Open3D/actions?query=workflow%3A%22macOS+CI%22)
[![Windows CI](https://github.com/intel-isl/Open3D/workflows/Windows%20CI/badge.svg)](https://github.com/intel-isl/Open3D/actions?query=workflow%3A%22Windows+CI%22)
[![Build Status](https://travis-ci.org/intel-isl/Open3D.svg?branch=master)](https://travis-ci.org/intel-isl/)

**Core features of Open3D include:**

* 3D data structures
* 3D data processing algorithms
* Scene reconstruction
* Surface alignment
* 3D visualization
* Physically based rendering (PBR)
* 3D machine learning support with PyTorch and TensorFlow
* GPU acceleration for core 3D operations
* Available in C++ and Python

For more, please visit the [Open3D documentation](http://www.open3d.org/docs).

## Python quick start

Pre-built pip and conda packages support Ubuntu 18.04+, macOS 10.14+ and
Windows 10 (64-bit) with Python 3.6, 3.7 and 3.8.

```bash
# Install Open3D stable release with pip
$ pip install open3d

# Install Open3D stable release with Conda
$ conda install -c open3d-admin -c conda-forge open3d

# Test the installation
$ python -c "import open3d as o3d; print(o3d)"

```

To get the latest features in Open3D, install the
[development pip package](http://www.open3d.org/docs/latest/getting_started.html#development-version-pip).
To compile Open3D from source, refer to
[compiling from source](http://www.open3d.org/docs/release/compilation.html).

## C++ quick start

Please refer to [compiling from source](http://www.open3d.org/docs/release/compilation.html)
and [Open3D C++ interface](http://www.open3d.org/docs/release/cpp_api.html).

## Open3D-Viewer app

<img width="480" src="https://raw.githubusercontent.com/intel-isl/Open3D/master/docs/_static/open3d_viewer.png">

Open3D-Viewer is a standalone 3D viewer app available on Ubuntu and macOS.
Please stay tuned for Windows. Download Open3D Viewer from the
[release page](https://github.com/intel-isl/Open3D/releases).

## Open3D-ML

<img width="480" src="https://raw.githubusercontent.com/intel-isl/Open3D-ML/master/docs/images/getting_started_ml_visualizer.gif">

Open3D-ML is an extension of Open3D for 3D machine learning tasks. It builds on
top of the Open3D core library and extends it with machine learning tools for
3D data processing. To try it out, install Open3D with PyTorch or TensorFlow and check out
[Open3D-ML](https://github.com/intel-isl/Open3D-ML).

## Communication channels

* [GitHub Issue](https://github.com/intel-isl/Open3D/issues): bug reports,
  feature requests, etc.
* [Forum](https://forum.open3d.org): discussion on the usage of Open3D.
* [Discord Chat](https://discord.gg/D35BGvn): online chats, discussions,
  and collaboration with other users and developers.

## Citation

Please cite [our work](https://arxiv.org/abs/1801.09847) if you use Open3D.

```bib
@article{Zhou2018,
    author    = {Qian-Yi Zhou and Jaesik Park and Vladlen Koltun},
    title     = {{Open3D}: {A} Modern Library for {3D} Data Processing},
    journal   = {arXiv:1801.09847},
    year      = {2018},
}
```
