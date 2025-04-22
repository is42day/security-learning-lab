FROM kalilinux/kali-rolling

# Install key security tools
RUN apt update && apt install -y \
    nmap \
    git \
    exploitdb \
    metasploit-framework \
    python3 python3-pip \
    vim tmux wget curl \
 && rm -rf /var/lib/apt/lists/*

# Clone Vulscan plugin for Nmap
RUN git clone https://github.com/scipag/vulscan /opt/vulscan

# Setup workspace
WORKDIR /workspace
