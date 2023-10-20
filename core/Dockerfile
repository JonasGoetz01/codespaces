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

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y

ENV PATH="/root/.cargo/bin:${PATH}"

RUN cargo --help