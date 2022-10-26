# Docker First

*Comando de build
 docker build -t elsonss/laravel .   

* Rodar imagem
  
  docker run --rm -it -p 8000:8000 --name laravel --mount type=volume,src=linuxtips,target="$(pwd)" --host 0.0.0.0 --port=8001  elsonss/laravel 
  
* Rodando na porta 8001 internamente e mapeando para  porta 8080
  
  docker run --rm -it -p 8000:8001 --name laravel --mount type=volume,src=linuxtips,target="$(pwd)" elsonss/laravel  --host=0.0.0.0 --port=8001

* Ver logs da porta
  docker logs laravel
