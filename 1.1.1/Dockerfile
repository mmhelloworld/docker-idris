FROM haskell:8

ARG stack_yaml
ADD $stack_yaml ./

RUN apt-get update && apt-get -y install build-essential pkg-config libffi-dev libgmp-dev && \
    stack install idris-1.1.1

ENV PATH="/bin/jdk/bin:/bin/idris-jvm/codegen/bin:${PATH}" 

CMD idris
