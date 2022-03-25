# Vacaciones

### Instalador del servicio vsftpd
`sudo apt-get update && sudo apt install vsftpd`

### Iniciamos y activamos el servicio
`sudo systemctl enable vsftpd`  
  
  
`sudo service vsftpd start`

### Comprobamos el estado
`sudo service vsftpd status`

### Crear certificado autofirmado
`sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/vsftpd.pem -out /etc/ssl/private/vsftpd.pem`

### Hacer una copia del archivo de configuración y añadir el modificado
`sudo mv /etc/vsftpd.conf /etc/vsftpd_back.conf`

**Copiar el archivo vsftpd.conf del repositorio**
`sudo nano /etc/vsftpd.conf`
