FROM debian:jessie

ENV HOME /home/app

RUN apt-get update && apt-get -y install --no-install-recommends \
    ca-certificates \
    curl \
    libglib2.0-0 \
	  libgl1-mesa-glx \
    libqt5gui5 \
    libx11-xcb1 \
	\
	&& rm -rf /var/lib/apt/lists/*

RUN mkdir -p $HOME/.config/robomongo \
    && groupadd -r app \
    && useradd -r -g app -G audio,video app

RUN curl -L "https://download.robomongo.org/1.2.1/linux/robo3t-1.2.1-linux-x86_64-3e50a65.tar.gz" -o robo3t.tar.gz \
    && tar -xvzf robo3t.tar.gz \
    && mv robo3t-1.2.1-linux-x86_64-3e50a65/* $HOME \
    && chown -R app:app $HOME \
    && rm -rf robo3t* \
    && ls -al

USER app

WORKDIR /home/app

ENTRYPOINT [ "/home/app/bin/robo3t" ]
