# Born2beRoot - peantoni - 42Lisboa

- **Arquivo do trabalho Born2beroot traduzido em PT-BR**
    
    [Borne2beRoot-Traduzido.pdf](https://github.com/PCallegaro/42_Born2beRoot/files/8645739/Borne2beRoot-Traduzido.pdf)

# Melhores guias para o projeto (Os que mais me ajudaram :D ):

    https://github.com/benmaia/42_Born2beRoot
    https://soraianovaes.notion.site/Born2beroot-d22e0203fc144c38a8f809f0432ee5d7

# Perguntas da avaliação:

- **Como funciona uma VM(Virtual Machine)?**
    
    Uma VM é um recurso que simula um ambiente computacional capaz de executar sistemas operacionais e programas como se fosse uma máquina física. Basicamente Um computador dentro de um computador.
    

- **Por que escolheu Debian ou CentOS e diferenças?**
    
    CentOS:
    
    -Considerado uso de maior parte empresarial, pelo fato de receber atualizações com pouca frequência, o que torna ele um sistema mais estável que o Debian.
    
    -Tem uma comunidade menor nas redes que o Debian, o que não permite muitos fóruns de ajuda para diversos problemas.
    
    -Tem uma quantidade menor de pacotes oferecidos comparado ao Debian, o que pode ser considerado uma vantagem para o Debian.
    
    -Não exige atualizações constantes e o suporte ao software é feito com uma visão de longo prazo.
    
    Debian:
    
    -Considerado para uma classe pessoal/doméstica visto que é utilizado pela maioria da comunidade nesse ambiente.
    
    -Menos estável que o CentOS, entretanto continua sendo muito estável, mesmo recebendo atualizações com muito mais frequência que o CentOS.
    
    -Quantidade de pacotes oferecidas é maior comparado ao CentOS.
    
    <img width="580" alt="Screen Shot 2022-05-07 at 6 34 09 PM" src="https://user-images.githubusercontent.com/83246404/167266847-78b658f0-814f-4155-ab5d-61a851947898.png">

    
    Fonte :[https://pt.education-wiki.com/9597652-centos-vs-debian](https://pt.education-wiki.com/9597652-centos-vs-debian)
    

- **Propósito das VM:**
    
    -O principal objetivo das VMs é possibilitar que sejam operados diversos sistemas operacionais ao mesmo tempo, a partir do mesmo hardware.
    

- **O que é APT:**
    
    Apt ou Advanced Packaging Tool é um software de código aberto e gratuito que lida com a instalação e remoção de software. Inicialmente, ele foi projetado para os pacotes `.deb` do Debian, mas tornou-se compatível com o RPM Package Manager.
    
    Apt é uma linha de comando inteira sem GUI. Sempre que invocado a partir da linha de comando junto com a especificação do nome do pacote a ser instalado, ele encontra esse pacote na lista configurada de fontes especificadas em '/etc/apt/sources.list' junto com a lista de dependências para aquele pacote e os classifica e os instala automaticamente junto com o pacote atual, permitindo que o usuário não se preocupe em instalar dependências.
    
    É altamente flexível, permitindo ao usuário controlar várias configurações facilmente, como: adicionar qualquer nova fonte para pesquisar pacotes, apt-pinning, ou seja, marcar qualquer pacote indisponível durante a atualização do sistema, tornando assim sua versão atual a sua versão final instalada, "inteligente" atualizar, ou seja, atualizar os pacotes mais importantes e deixar os menos importantes.
    

- **O que é Aptitude:**
    
    Aptitude é um front-end para uma ferramenta de empacotamento avançada que adiciona uma interface de usuário à funcionalidade, permitindo ao usuário pesquisar interativamente por um pacote e instalá-lo ou removê-lo. Criado inicialmente para Debain, o Aptitude estende sua funcionalidade para distribuições baseadas em RPM também.
    
    Sua interface de usuário é baseada na biblioteca ncurses, que adiciona vários elementos comumente vistos em GUIs. Um de seus destaques é que ele pode emular a maioria dos argumentos de linha de comando do apt-get.
    
    Ao todo, o Aptitude é um gerenciador de pacotes de nível superior que abstrai detalhes de baixo nível e pode operar tanto no modo de IU interativo baseado em texto quanto no modo não interativo de linha de comando.
    

- **Diferenças entre APT e Aptitude:**
    
    O Apt-get sendo um gerenciador de pacotes de nível inferior é restrito apenas à linha de comando, enquanto o Aptitude sendo uma ferramenta de nível superior possui uma interface interativa padrão somente de texto junto com a opção de operação de linha de comando digitando os comandos necessários.
    

- **O que é AppArmor?**
    
    AppArmor é um módulo de segurança do kernel do Linux que permite ao administrador do sistema restringir os recursos dos programas com perfis por programa. Os perfis podem permitir recursos como acesso à rede, acesso a soquete bruto e permissão para ler, gravar ou executar arquivos em caminhos correspondentes.
    

- **O que é SSH e como funciona?**
    
    O SSH(*Secure Socket Shell)* é um protocolo de rede para o usuário internet acessar, administrar e modificar  remotamente seus servidores. Isso inclui gerenciamento de contas de hospedagem que usam, por exemplo, serviços de VPS.
    
    Tudo isso acontece pela rede. Nesta situação, dados, informações, documentos e arquivos são alcançados pelo usuário através de uma comunicação criptografada entre máquinas (o computador do usuário) e servidores (de hospedagem).
    
    O que acontece é que essa comunicação contém um mecanismo de autenticação. Nele, é aplicada uma tecnologia de criptografia avançada que mascara os dados e transações de quem está acessando até o quê exatamente está se querendo acessar.
    

- **O que é LVM?**
    
    LVM é um método de alocar espaço do disco rígido em volumes lógicos que podem ser facilmente redimensionados, ao contrário das partições.
    
    Com o LVM, o disco rígido ou conjunto de discos rígidos é alocado em um ou mais *volumes físicos*. Um volume físico não pode ultrapassar mais de um disco.
    
    Os volumes físicos são combinados em *grupos de volume lógico*, com exceção da partição /boot/. A partição /boot/ não pode estar em um grupo de volume lógico porque o gestor de início não pode acessá-lo. Se a partição root / estiver em um volume lógico, crie uma partição /boot/ separada, que não seja parte de um grupo de volume.
    
    Já que um volume físico não pode ultrapassar mais de um disco, crie um ou mais volumes físicos por disco para poder ultrapassar este limite.
    

- **O que é Cron e Crontab?**
    
    Esses dois comandos são, de uma maneira geral, os responsáveis pelo agendamento e execução de tarefas que o usuário espera que sejam executadas com certa regularidade. Essa constância pode ser várias vezes por minuto, hora, dia, mês ou ano. Com toda a vantagem que os scripts possibilitam em qualquer linguagem que seja escrito, todas as possibilidades se tornam praticamente infinitas.
    
    Suponha que você precise fazer um backup de seu banco de dados MySQL, todos os dias as 6 horas da manhã. Não seria mais viável que o próprio Linux fizesse esse backup automaticamente para você? É esse tipo de comodidade que o Cron permite que você tenha. Além disso, é muito simples e basta criar um script e agendar no arquivo Crontab para que o backup seja executado todos os dias na hora estipulada por você.

<hr>

- **Links Uteis**
    
    https://soraianovaes.notion.site/Born2beroot-d22e0203fc144c38a8f809f0432ee5d7
    
    https://pt.linux-console.net/?p=1375
    
    https://pt.education-wiki.com/9597652-centos-vs-debian
    
    https://www.weblink.com.br/blog/tecnologia/acesso-ssh-o-que-e/
    
    https://web.mit.edu/rhel-doc/3/rhel-sag-pt_br-3/ch-lvm-intro.html
    
    https://www.isbrasil.info/blog/o-que-e-cron-e-crontab.html
    
    https://github.com/benmaia
    
