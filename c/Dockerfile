FROM jonasgoetz01/codespaces-base:latest

RUN apt update && \
	apt dist-upgrade -y && \
	apt full-upgrade

RUN apt install build-essential -y

COPY .zsh_aliase /root/.zsh_aliase

RUN cat ~/.zsh_aliase >> ~/.zshrc

RUN apt install clang -y

RUN python3 -m pip install --upgrade pip setuptools && \
	python3 -m pip install norminette

RUN pip3 install c_formatter_42

RUN apt-get -y install sudo

RUN apt-get install -y lsb-release

RUN apt-get install python-dev-is-python3 -y

RUN apt install python3.10-venv -y

RUN zsh -c "$(curl -fsSL https://raw.github.com/xicodomingues/francinette/master/bin/install.sh)" | true