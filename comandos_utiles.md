
* **Conexión ssh:**   
sudo ssh -i icemd.pem ubuntu@ec2-18-202-243-222.eu-west-1.compute.amazonaws.com

* **Subir fichero a EC2:**    
scp -i icemd.pem datos.csv ubuntu@ec2-18-202-243-222.eu-west-1.compute.amazonaws.com
 
* **Bajar fichero a EC2:**   
	scp -r -i icemd.pem ubuntu@ec2-18-202-243-222.eu-west-1.compute.amazonaws.com . 

* **Log de instalaciones previas:**   
	/var/log/cloud-init-output.log 

* **Instalar miniconda3:**   
	curl -O https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh  
	bash Miniconda3-latest-Linux-x86_64.sh

* **Exportar entorno conda:**    
	conda list --explicit > spec-file.txt

* **Crear entorno conda a partir de spec-file.txt:**   
	conda create --name myenv --file spec-file.txt

* **Override sudo:**   
	sudo() { command sudo env PATH="$PATH" "$@"; }

* **HTTP POST Request:**   
	curl -H "Content-Type: application/json" -d "@query.json" -X POST http://0.0.0.0:9999/predict

        


