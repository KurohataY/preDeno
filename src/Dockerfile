FROM centos:8

WORKDIR /preDeno
COPY ./ ./

RUN dnf -y install langpacks-ja unzip
RUN export LC_ALL=C
RUN curl -fsSL https://deno.land/x/install/install.sh | sh
ENV DENO_INSTALL="/root/.deno"
ENV PATH="$DENO_INSTALL/bin:$PATH"
RUN deno run https://deno.land/std/examples/welcome.ts
RUN deno install --allow-net --unstable https://deno.land/x/vno/install/vno.ts

