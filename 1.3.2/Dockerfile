FROM haskell:8.6.5

ARG stack_yaml
ADD $stack_yaml ./

ENV LD_LIBRARY_PATH=/opt/ghc/8.6.5/lib/ghc-8.6.5/rts:$LD_LIBRARY_PATH

RUN apt-get update && apt-get -y install build-essential pkg-config libffi-dev libgmp-dev && \
    stack install idris-1.3.2

ENV PATH="/bin/jdk/bin:/bin/idris-jvm/codegen/bin:${PATH}"

CMD idris
