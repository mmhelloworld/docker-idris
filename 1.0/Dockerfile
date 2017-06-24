FROM haskell:8

RUN apt-get update && apt-get -y install build-essential pkg-config libffi-dev libgmp-dev && stack install idris

ENV PATH="/bin/jdk/bin:/bin/idris-jvm/codegen/bin:${PATH}" 

CMD idris
