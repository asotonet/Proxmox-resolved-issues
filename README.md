# Proxmox-resolved-issues

##Verifica el soporte de Proxmox
Si estás usando Proxmox, asegúrate de que el contenedor se esté ejecutando con los permisos adecuados en un LXC o VM. En algunos casos, es necesario habilitar opciones como "Privileged Container" o modificar los permisos en Proxmox.

Para LXC, edita el archivo de configuración del contenedor (/etc/pve/lxc/<id>.conf) y agrega:

bash´´´
lxc.apparmor.profile: unconfined
lxc.cap.drop:
´´´
Luego reinicia el contenedor.
