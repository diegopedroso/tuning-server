Playbook para Tuning de Kernel das máquinas do FIBRE

Requirements
------------

Ansible 2.5.5 ou superior.


Contém as seguintes Roles:

System
=========
Essa role realiza configurações de S.O e rede no arquivo sysctl.

Locale
=========
Essa role configura a localidade das instancias PT ou EN.


Role Variables
=========
    

    #swap
    swapfile_location: /swapfile

    #swapfile_size: "2G"
    swapfile_size: 1

    #swappiness this control is used to define how aggressively the kernel swaps out anonymous memory relative to pagecache and other caches. Increasing the value increases the amount of swapping. The default value is 60.
    swapfile_swappiness: 0

    #vfs_cache_pressure this variable controls the tendency of the kernel to reclaim the memory which is used for caching of VFS caches, versus pagecache and swap. Increasing this value increases the rate at which VFS caches are reclaimed.
    swapfile_vfs_cache_pressure: 50

    #if set to False, fallocate is used to create the swapfile, otherwise, dd is used. You may need to set this to True if your filesystem does not support fallocate
    swapfile_use_dd: False

    #Kernel
    #Controls the kernel's behavior when a hung task is detected.This file shows up if CONFIG_DETECT_HUNG_TASK is enabled. //0: continue operation. This is the default behavior.//1: panic immediately.
    kernel_hung_task_panic: 0

    #Should the soft-lockup detector generate panics.
    kernel_softlockup_panic: 10

    #When set to 1 the kernel will panic on OOM.A setting of 0 instructs the kernel to call a function named oom_killer on an OOM. Usually, oom_killer can kill rogue processes and the system will survive.
    vm_panic_on_oom: 0

    #[KNL] Kernel behaviour on panic: delay <timeout>/timeout > 0: seconds before rebooting/timeout = 0: wait forever/timeout < 0: reboot immediately
    kernel_panic: 15


Packages
=========
Essa role realiza a instalação de pacotes básicos nas instâncias.


Python
=========
<<<<<<< HEAD
Essa role instala a versão minima do Python.
=======
<<<<<<< HEAD
Essa role instala o Python minimal.
=======
Essa role instala o python minimal.
>>>>>>> 7fcdf0d... chore/ READ update
>>>>>>> 2faf4ed4709762aa4a89ea27c7815a0f8d4031b1


Limits
=========
Essa role configura os limites de processos e abertura de arquivos por usuário, além da quantidade maxima de endereços bloqueados na memória.
