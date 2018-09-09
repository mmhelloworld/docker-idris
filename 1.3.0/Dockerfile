FROM haskell:8.2

ARG stack_yaml
ADD $stack_yaml ./

RUN stack upgrade --binary-version 1.6.3
RUN apt-get update && apt-get -y install build-essential pkg-config libffi-dev libgmp-dev && \
    stack install idris-1.3.0

ENV PATH="/bin/jdk/bin:/bin/idris-jvm/codegen/bin:${PATH}"

CMD idris
