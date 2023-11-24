FROM ubuntu:latest

RUN apt update && apt upgrade -y

RUN apt install curl -y

RUN apt install nano -y

RUN apt install exa -y

RUN apt install wget -y

RUN apt install zsh -y

RUN apt install python3 -y && \
	apt install python3-pip -y

RUN apt-get install python-dev-is-python3 -y

RUN apt install python3.10-venv -y


RUN apt install git -y
RUN git config --global user.name "vsivanat" && \
	git config --global user.email "vsivanat@student.42.fr"

RUN apt install build-essential -y 

RUN apt install lsb-release -y

RUN apt install sudo -y

COPY .zsh_aliase /root/.zsh_aliase

RUN wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh && \
	chmod 755 install.sh && \
	./install.sh && \
	rm install.sh

RUN chsh -s zsh

RUN cat ~/.zsh_aliase >> ~/.zshrc

COPY .nanorc /root/.nanorc

RUN python3 -m pip install --upgrade pip setuptools && \
	python3 -m pip install norminette

RUN bash -c "$(curl -fsSL https://raw.github.com/xicodomingues/francinette/master/bin/install.sh)"

CMD ["zsh"]