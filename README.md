Using the technique from:
https://github.com/resin-io-projects/armv7hf-debian-qemu

Wrap your build steps to taint the environment with qemu allowing building on x86_64.
```
RUN [ "cross-build-start" ]
RUN echo do buid steps here
RUN [ "cross-build-end" ]
```

This leaves the container as a pure ARM container that could be pulled on a raspberry pi