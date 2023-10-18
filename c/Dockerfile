FROM jonasgoetz01/codespaces-base:latest

RUN apt update && \
	apt dist-upgrade -y && \
	apt full-upgrade

RUN apt install build-essential -y

COPY .zsh_aliase /root/.zsh_aliase

RUN cat ~/.zsh_aliase >> ~/.zshrc
