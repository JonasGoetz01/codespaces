FROM jonasgoetz01/codespaces-base:latest

RUN apt update && \
	apt dist-upgrade -y && \
	apt full-upgrade

COPY .zsh_aliase /root/.zsh_aliase

RUN cat ~/.zsh_aliase >> ~/.zshrc

RUN apt-get -qq update

RUN apt-get install -y -q \
    build-essential

RUN curl https://sh.rustup.rs -sSf | sh -s -- -y

ENV PATH="/root/.cargo/bin:${PATH}"

RUN cargo --help
