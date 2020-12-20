FROM haskell:8.8.4

ARG stack_yaml
ADD $stack_yaml ./

ENV LD_LIBRARY_PATH=/opt/ghc/8.8.4/lib/ghc-8.8.4/rts:$LD_LIBRARY_PATH

RUN apt-get update && apt-get -y install build-essential pkg-config libffi-dev libgmp-dev && \
    stack install idris-1.3.3

ENV PATH="/bin/jdk/bin:/bin/idris-jvm/codegen/bin:${PATH}"

CMD idris
