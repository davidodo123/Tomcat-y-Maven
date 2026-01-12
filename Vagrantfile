Vagrant.configure("2") do |config|
  config.vm.box = "debian/bullseye64"
  config.vm.network "private_network", ip: "192.168.56.10"

  # Redirección de puerto para acceder a Tomcat desde tu navegador
  config.vm.network "forwarded_port", guest: 8080, host: 8080

  # Sincroniza el directorio local
  config.vm.synced_folder ".", "/vagrant", disabled: false

  # COMENTA O ELIMINA LA LÍNEA DE NGINX PARA EVITAR ERRORES
  # config.vm.synced_folder "./web", "/var/www/juanma-davids.test/html", ...

  # Provisionamiento (si vas a usar el script bootstrap.sh)
  # config.vm.provision "shell", path: "bootstrap.sh"
end