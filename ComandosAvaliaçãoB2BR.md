- **Comandos para Avaliação**
    
    ### Check signature
    
    ```bash
    cd /Users/Peantoni/VirtualBox VMs/Debian10
    certUtil -hashfile debian10.vdi sha1
    ```
    
    ### Simple Setup
    
    ```bash
    sudo aa-status                   <- AppArmor status
    sudo service ssh status          <- ssh status, yep
    systemctl status sshd            <- ssh status
    sudo ufw status                  <- ufw status
    cat /etc/os-release              <- checar OS instalado com versão
    uname -v                         <- checar sistema operacional
    ```
    
    ### User
    
    ```bash
    getent group sudo                <- sudo group users
    getent group user42              <- user42 group users
    cat /etc/passwd                  <- ver todos os usuários do sistema
    ```
    
    ### Create a new user
    
    ```bash
    sudo adduser username <- creating new user (yes (no))
    sudo chage -l username  <- Verify password expire info for new user
    sudo adduser username sudo
    sudo chage -n 2 username <- aplicar políticas de senha ao usuário que já existe
    sudo chage -M 30 username <- aplicar políticas de senha ao usuário que já existe
    sudo userdel
    sudo adduser username user42  <- assign new user to sudo and user42 groups
    sudo groupadd groupname <- criar grupo
    sudo usermod -aG groupname username <- add user ao grupo
    vim /etc/login.defs             <- password expire policy
    vim /etc/pam.d/common-password  <- password policy
    ```
    
    ### Hostname
    
    ```bash
    hostname                         <- nome host
    sudo vim /etc/hostname          <- trocar hostname
    sudo vim /etc/hosts             <- trocar hostname não usar
    sudo hostnamectl set-hostname snovaes42 <- trocar hostname
    sudo reboot
    lsblk                            <- Check partitions
    ```
    
    ### Sudo
    
    ```bash
    sudo visudo                      <- regras sudo
    sudo adduser username user42  <- assign new user to sudo and user42 groups
    cat log <- Input log
    cat ttyout <- Output log
    ```
    
    ### UFW
    
    ```bash
    sudo ufw status
    sudo ufw allow 8080
    sudo ufw delete allow 8080
    ```
    
    ### SSH
    
    ```bash
    ip a                             <- ip adress
    ssh -p 4242 peantoni-@127.0.0.1 -p    <- connect to VM from your host (physical)machine via sudSSH
    vim /etc/sudoers.d/
    You can $ ls /etc/sudoers.d
    ssh snovaes@192.168.1.114        <- testar se abre qualquer porta
    ssh root@192.168.1.114 -p 4242   <- testar se loga pelo root
    ```
    
    ### CRON
    
    ```bash
    sudo crontab -l                  <- cron schedule
    sudo crontab -u root -e          <- edit rules (ver manual)
    cd /var/spool/cron/crontabs/     <- file root rules
    sudo service cron stop/start     <- stop and start cron
    sudo service cron disable        <- desabilita o serviço mesmo reiniando a VM
    sudo service cron enable         <- habilita o serviço
    sudo service cron restart        <- restart
    sudo service cron status         <- status
    
    sudo vim /usr/local/bin/monitoring.sh <- ver monitoring
    sudo cat /etc/network/interfaces <- ver ip estático
    sudo poweroff
    sudo reboot
    ```
