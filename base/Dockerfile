FROM ubuntu:bionic
RUN apt update; apt install -y git make
RUN git clone https://github.com/getfem-doc/getfem.git
WORKDIR getfem
RUN apt-get install -y --no-install-recommends automake
RUN apt-get install -y --no-install-recommends libtool
RUN apt-get install -y --no-install-recommends make
RUN apt-get install -y --no-install-recommends g++
RUN apt-get install -y --no-install-recommends libqd-dev
RUN apt-get install -y --no-install-recommends libqhull-dev
RUN apt-get install -y --no-install-recommends libmumps-seq-dev
RUN apt-get install -y --no-install-recommends liblapack-dev
RUN apt-get install -y --no-install-recommends libopenblas-dev
RUN apt-get install -y --no-install-recommends libpython3-dev
RUN apt-get install -y --no-install-recommends ufraw
RUN apt-get install -y --no-install-recommends imagemagick
RUN apt-get install -y --no-install-recommends fig2dev
RUN apt-get install -y --no-install-recommends texlive
RUN apt-get install -y --no-install-recommends xzdec
RUN apt-get install -y --no-install-recommends fig2ps
RUN apt-get install -y --no-install-recommends gv
RUN apt-get install -y --no-install-recommends python3-pip
RUN pip3 install -r requirements.txt
RUN bash autogen.sh
RUN ./configure --with-pic
RUN make -j8
RUN make -j8 check
RUN make install
