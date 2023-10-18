FROM ubuntu:22.04

RUN apt update && \
	apt dist-upgrade -y && \
	apt full-upgrade -y

RUN apt install curl -y

RUN apt install nano -y

RUN apt install zsh -y

RUN apt install exa -y

RUN apt install wget -y

RUN apt install git -y

RUN apt install python3 -y && \
	apt install python3-pip -y

RUN git config --global user.name "jgotz" && \
	git config --global user.email "jonas.goetz01@web.de"

RUN apt install sed -y

RUN sed -i 's|/bin/bash|/bin/zsh|' /etc/passwd

RUN wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh && \
	chmod 755 install.sh && \
	./install.sh && \
	rm install.sh

COPY .nanorc /root/.nanorc

COPY .zsh_aliase /root/.zsh_aliase

RUN cat ~/.zsh_aliase >> ~/.zshrc

CMD ["/bin/zsh"]
