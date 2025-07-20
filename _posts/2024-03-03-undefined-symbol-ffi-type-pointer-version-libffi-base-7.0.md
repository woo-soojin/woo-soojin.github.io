---
layout: post
title: undefined symbol: ffi_type_pointer, version LIBFFI_BASE_7.0
# summary: Markdown is a way to style text on the web. You control the display of the document; formating words as bold or italic, adding images, and creating lists are just a few of the things we can do with Markdown. Mostly, Markdown is just regular text with a few non-alphabetic characters thrown in.
# featured-img: how-to-install-ros-kinetic
# categories: ROS
featured-img: emile-perron-190221
categories: Linux
---

### undefined symbol: ffi_type_pointer, version LIBFFI_BASE_7.0 Error Message from cv_bridge.boost.cv_bridge_boost import getCvType ImportError: /usr/lib/x86_64-linux-gnu/libp11-kit.so.0: undefined symbol: ffi_type_pointer, version LIBFFI_BASE_7.0 Solution conda activate test_env 

```
conda install libffi==3.3
```