## Configuração para 75 Hz no Ubuntu 

**75 Hz resulta em 74.99 Hz**.

**74.97 Hz** (diferença de apenas **0.02 Hz**, imperceptível).

### 1. Edite o GRUB

```bash
sudo nano /etc/default/grub
```


Altere a linha para:
```bash
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash amdgpu.dc=1 amdgpu.gpu_recovery=1 video=DP-1:1920x1080M@75"
```


Salve com:

Ctrl + O
Enter
Ctrl + X

Atualize o GRUB
```bash
sudo update-grub
sudo reboot
```
